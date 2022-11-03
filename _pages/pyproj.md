---
layout: page
title: pyproj
order: 10
---

*pyproj* er et grensesnitt til Proj for Python. pyproj er et anbefalt API ettersom det bruker å være oppdatert med siste versjon av Proj. API'et kan brukes både i kommando og i pythonscripts.

* [Dokumentasjon på pyproj](https://pyproj4.github.io/pyproj/stable/)
* [pyproj på GitHub](https://github.com/pyproj4/pyproj)

### Installasjon av pyproj ved conda

> conda config --prepend channels conda-forge \
> conda config --set channel_priority strict \
> conda install pyproj

### Installasjon av pyproj med pip

> pip install pyproj

Kommando for å vise installert versjon:

> pyproj

Laste ned ressursfiler for norske områder med pyproj:

> pyproj sync --bbox 2,57,32,82

Ressursfilene vil plasseres i samme mappe som for standard Proj-installasjon.

#### Hente info om koordinatsystem

> python \
> from pyproj import CRS # (NGO48 geografisk) \
> crs_4273 = CRS.from_epsg(4273)

#### Transformere mellom to koordinatsystemer

> python \
> from pyproj import Transformer, transform \
> transform = Transformer.from_crs(4258, 4273) # Transformerer fra EUREF89 geogr. til NGO48 geogr. \
> transform.transform(60,10,0,2020) \
(59.99924756384341, 10.004772119609207, 0.0, 2020.0)

#### Transformere til projeksjon som mangler EPSG-kode

> python \
> from pyproj import Transformer, transform \
> transform = Transformer.from_crs(7789, "+proj=utm +zone=32 +ellps=GRS80") # Transformerer fra ITRF2014 jordsentrisk til ITRF2014 UTM32 \
> transform.transform(2345766.37502,543139.33223,5886461.69393,2020.00)

#### Transformasjon mellom ulike epoker i samme referanseramme med hastighetsmodell

> python \
> from pyproj import Transformer, transform \
> transform = Transformer.from_pipeline("+proj=deformation +t_epoch=2000.0 +grids=eur_nkg_nkgrf17vel.tif") # Transformerer til epoke 2000.0 \
> transform.transform(2345766.37502, 543139.33223, 5886461.69393, 2020.00)

#### Eksempel på transformasjon med *proj-streng* i *pyproj*

I dette eksempelet blir proj-strengen satt opp til å transformere mellom to forskjellige ellipsoider.

> python \
> from pyproj import Transformer, transform \
> projline_str = ( \
>     "+proj=pipeline" \
>     "+step +proj=axisswap +order=2,1" \
>     "+step +proj=unitconvert +xy_in=deg +z_in=m +xy_out=rad +z_out=m" \
>     "+step +proj=cart +ellps=GRS80" \
>     "+step +inv +proj=cart +a=6378136.0 +rf=298.25784" \
>     "+step +proj=unitconvert +xy_in=rad +z_in=m +xy_out=deg +z_out=m" \
>     "+step +proj=axisswap +order=2,1" \
> )
