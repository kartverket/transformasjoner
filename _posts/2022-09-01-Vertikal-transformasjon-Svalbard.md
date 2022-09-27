---
layout: post
title: Vertikal transformasjon på Svalbard
author: Sveinung Himle
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

I den siste versjonen av Proj kan man nå transformere mellom ETRS89 ellipsoidiske høyder og det vertikale høydedatumet SVD2006.	

### Nye EPSG-koder

Det vertikale datumet *SVD2006* har fått tildelt EPSG-koden *EPSG:20000*. Koden ved sammensetting med det horisontale datumet ETRS89 2D lat/lon 
er *EPSG:20001*.

### Eksempel transformasjon fra ETRS89 2D lat/lon til SVD2006

```
cs2cs -d 4 EPSG:4258 EPSG:20001
80.0000 22.0000 100.0000
80.0000 22.0000 72.1528
```

### Nedlasting av ressursfil

Ressursfilene som transformasjonen er avhengig av er sleppt på [cdn.proj.org](https://cdn.proj.org) og [PROJ-data](https://github.com/OSGeo/PROJ-data).


Link til høydereferansemeoll på dette repoet:

* [Korreksjonsgridd ITRF2014-EUREF89](https://github.com/kartverket/transformasjoner/tree/master/src/projresources/public/no_kv_arcgp-2006-sk.tif)


Kopier fila til aktuell ressursmappe		

Med Windows:

```
c:\User\< username >\AppData\Local\proj
```

Med Linux:

```
/.local/share/proj
```
