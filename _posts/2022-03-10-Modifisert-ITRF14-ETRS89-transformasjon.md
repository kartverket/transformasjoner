---
layout: post
title: Modifisert transformasjon mellom ITRF2014 og EUREF89
author: Sveinung Himle
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

Kartverket har publisert en modifisert transformasjon mellom ITRF2014 og EUREF89. Den modifiserte transformasjonen er bedre tilpasset Landsnettet enn den første versjonen.
I praksis vil det bety at man vil treffe bedre om man transformerer en ITRF2014-løsning av et landsnettspunkt til EUREF89. Avviket mellom første og siste transformasjon er vel 1 cm i nordretning for Finnmark, 
men avtar sørover.

Foreløpig er ikke den modifiserte transformasjonen sleppt på [cdn.proj.org](https://cdn.proj.org) og [PROJ-data](https://github.com/OSGeo/PROJ-data), men det ventes at transformasjonen være inkludert i neste versjon av PROJ-data (PROJ-data 2.0).

Transformasjonen ITRF2014 mellom EUREF89 består blant annet av et korreksjonsgridd med jordsentriske translasjoner (X, Y og Z). Griddet er på GeoTIFF-format og den siste versjonen ligger klar til
nedlasting i dette repoet.


Link til korreksjonsgridd på dette repoet:

* [Korreksjonsgridd ITRF2014-EUREF89](https://github.com/kartverket/transformasjoner/tree/master/src/projresources/public/no_kv_NKGETRF14_EPSG7922_2000.tif)


Kopier fila til aktuell ressursmappe		

Med Windows:

```
c:\User\< username >\AppData\Local\proj
```

Med Linux:

```
/.local/share/proj
```
