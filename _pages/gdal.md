---
layout: page
title: GDAL
order: 11
---

GDAL er et "open source"-bibliotek for rasteroperasjoner.  

* [Link til GDAL si nettside](https://gdal.org/)
* [GDAL på Github](https://github.com/OSGeo/gdal)

### Installasjon av GDAL med Conda

> conda create --name gdal \
> conda activate gdal \
> conda install -c conda-forge gdal

Ved installasjon av GDAL vil Proj bli installert samtidig. For å sikre at norske transformasjoner fungerer bør man synkronisere (laste ned) ressursfilene som er aktuelle for Norge.

Laste ned ressursfiler for norske områder:
> projsync --bbox 2,57,32,82

Dersom alle ressursfiler skal lastes ned så kjør:
> projsync --all

### Transformasjon av enkeltpunkter med GDAL

> gdaltransform -s_srs EPSG:7912 -t_srs EPSG:4937 \
Enter X Y [Z [T]] values separated by space, and press Return. \
10 60 100 2020 \
9.99999191488498 59.9999951095245 99.86624677293

### Transformasjon av raster

> gdalwarp -s_srs EPSG:25833 -t_srs EPSG:25832 input.tif output.tif

### Transformasjon av filer

GDAL har støtte for konvertering, transformering og formatering av en mengde ulike vektor formater [Link til vektorformater som det er støtte for i GDAL](https://gdal.org/drivers/vector/index.html).

Eksempel på transformasjon fra NN42 til NN2000 på GML i EUREF89 UTM32:
>ogr2ogr -t_srs EPSG:5972 -s_srs EPSG:6172 -f GML Utfil_EPSG5972.gml Innfil_EPSG6172.gml

