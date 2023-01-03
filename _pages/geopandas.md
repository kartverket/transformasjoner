---
layout: page
title: GeoPandas
order: 12
---

GeoPandas er et "open source"-bibliotek for Python og en utvidelse av Pandas. PyProj følger med installasjon av GeoPandas og det gjør biblioteket egnet for transformasjon av diverse filformater.

### Eksempel på filformater som det er støtte for i GeoPandas.

* Shape
* GeoJson
* GeoPackage

### Linker til GeoPandas.

* [Link til GeoPandas si nettside](https://geopandas.org/en/stable/)
* [GeoPandas på Github](https://github.com/geopandas/geopandas)

### Installasjon av GeoPandas med pip

> pip install geopandas 

### Eksempel trransformasjon av shape-fil

```
import geopandas

data = geopandas.read_file('InnData.shp') # inndata i EPSG:25833
data = data.to_crs(epsg=5973)
data.to_file('UtData.shp') #utdata i EPSG:5973
```
