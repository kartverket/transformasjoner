---
layout: page
title: pyproj
order: 9
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
