---
layout: page
title: Transformasjon med EPSG-koder
order: 6
---

Transformasjonene og referanserammene i Proj følger kodene i EPSG-registeret. EPSG-registeret er administrert av IOGP (International Association of Oil & Gas Producers) og fungerer som en "de facto standard" vedrørende transformasjoner og referanserammer.		

Transformasjoner med EPSG-koder er en enkel og anbefalt alternativ metodikk. Brukeren og systemene trenger da bare forholde seg til kodene som er gitt for referanserammene og transformasjonene.		

Det mest vanlig vil være å oppgi EPSG-kodene på referanserammen/koordinatsystemet man skal transformere fra og til.		

## Linker til EPSG

* [EPSG-registeret](https://epsg.org/home.html)
* [Søkeside på EPSG-koder fra MapTiler Team](https://epsg.io/)
* [EPSG-koder i GeoNorge](https://register.geonorge.no/epsg-koder)

## Norske ref.rammer/koordinatsystemer støtta av Proj

| Namn ref.rammer                 | Autoritet | Kode        | Merknad                          |
| ------------------------------- | --------- | ----------- | -------------------------------- |
| ETRS89 geogr. NN2000            | EPSG      |        5942 | Sammensett 2D + 1D               |
| ETRS89 geogr. NN54              | EPSG      |        6144 | Sammensett 2D + 1D               |
| ETRS89 2D geogr.                | EPSG      |        4258 |                                  |
| ETRS89 3D geogr.                | EPSG      |        4937 |                                  |
| ETRS89 geosentrisk              | EPSG      |        4936 |                                  |
| ETRS89 UTM 31-36 2D             | EPSG      | 25831-25836 |                                  |
| ETRS89 UTM 31-36 NN54           | EPSG      |   6171-6176 | Sammensett 2D + 1D               |
| ETRS89 UTM 31-36 NN2000         | EPSG      |   5971-5976 | Sammensett 2D + 1D               |
| ETRS89 NTM 5-30 2D              | EPSG      |   5105-5130 |                                  |
| ETRS89 NTM 5-30 NN54            | EPSG      |   6145-6170 | Sammensett 2D + 1D               |
| ETRS89 NTM 5-30 NN2000          | EPSG      |   5945-5970 | Sammensett 2D + 1D               |
| NN2000                          | EPSG      |        5941 | Vertialt datum. Bruk heller 5942 |
| NN54                            | EPSG      |        5776 | Vertialt datum. Bruk heller 6144 |
| ETRS89 geogr. 3D Norway Heights | EPSG      |        5942 |                                  |
| CD Norway Depths                | EPSG      |        9672 | (Sjøkartnull). Bruk heller 9883  |
| ETRS89 geogr. 3D CD Norway      | EPSG      |        9883 | Sammensett 2D + 1D               |
| NGO48 geografisk 2D             | EPSG      |        4273 |                                  |
| NGO48 akse I-VIII               | EPSG      | 27391-27398 |                                  |
| ITRF2014 geosentrisk            | EPSG      |        7789 |                                  |
| ITRF2014 geogr. 2D              | EPSG      |        9000 |                                  |
| ITRF2014 geogr. 3D              | EPSG      |        7912 |                                  |
| ED50                            | EPSG      |        4230 | Under arbeid                     |
| ED50 UTM 31-36 2D               | EPSG      | 23031-23036 | Under arbeid                     |


### Tilgjengelig transformasjoner (eksempler)

| Transformasjon                             | Fra kode            | Til kode       | Kode - area |
| ------------------------------------------ | ------------------- | -------------- | ----------- |
| ETRS89 geogr. ell > ETRS89 geogr. NN54     | EPSG:4258/EPSG:4937 |      EPSG:6144 |             |
| ETRS89 geogr. ell > ETRS89 geogr. NN2000   | EPSG:4258/EPSG:4937 |      EPSG:5942 |             |
| ETRS89 geosentrisk > ITRF2014 geosentrisk. |           EPSG:4936 |      EPSG:7789 |   EPSG:1352 |
| ETRS89 UTM32 > NGO48 III                   |          EPSG:25831 |     EPSG:27391 |             |


### Benchmarktesting av punkter med Proj

I tabellen nedenfor vilkårlige punkter transformert i Proj med EPSG-koder på fra- og til-koordinatsystemet. Resultatet her kan gjerne brukes ved enhetstesting ved bruk av Proj.

| Fra kode   | Til kode   | Input X/lon/E  | Input Y/lat/N | Input Z/h/H    | Epoke    | Output X/lon/E  | Output Y/lat/N  | Output Z/h/H    | Områdekode |
| ---------- | ---------- | -------------- | ------------- | -------------- | -------- | --------------- | --------------- | ----------------| ---------- | 
|  EPSG:7789 |  EPSG:4936 |  1874722.01378 |  912943.23060 |  6007499.79547 |  2020.00 |  1874722.630745 |   912942.993045 |  6007499.590605 |          - |
|  EPSG:4937 |  EPSG:4273 |         10.000 |        60.000 |              - |        - | 10.004772119609 | 59.999247563843 |               - |          - |
| EPSG:25832 | EPSG:27393 |     500000.000 |   6600000.000 |              - |        - |     -97197.1595 |     172511.9003 |               - |          - |
|  EPSG:4230 |  EPSG:4326 |         10.000 |        60.000 |              - |        - |  9.998594123185 | 59.999544266822 |               - |          - |
|  EPSG:4230 |  EPSG:4326 |          3.000 |        60.000 |              - |        - |  2.998327769141 | 59.999460761204 |               - |          - |
|  EPSG:4258 |  EPSG:5941 |         12.000 |        60.000 |        100.000 |        - |          12.000 |          60.000 |       64.266998 |          - |
|  EPSG:4937 |  EPSG:5776 |         12.000 |        60.000 |        100.000 |        - |          12.000 |          60.000 |       64.054001 |          - |
| EPSG:25832 |  EPSG:5972 |     500000.000 |   6600000.000 |        100.000 |        - |      500000.000 |     6600000.000 |       58.042431 |          - |
| EPSG:25832 |  EPSG:6172 |     500000.000 |   6600000.000 |        100.000 |        - |      500000.000 |     6600000.000 |       58.039824 |          - |
|  EPSG:4258 |  EPSG:4230 |         10.000 |        60.000 |              - |        - | 10.001392846773 | 60.000445365016 |               - |  EPSG:1182 |
|  EPSG:7912 |  EPSG:4937 |         10.000 |        60.000 |        100.000 |  2020.00 |  9.999991896247 | 59.999995111756 |       99.866516 |          - |
|  EPSG:7912 |  EPSG:4937 |         10.000 |        60.000 |        100.000 |  2010.00 |  9.999994703625 | 59.999996480391 |       99.913775 |          - |
|  EPSG:4937 |  EPSG:9883 |          5.040 |        60.100 |         40.000 |        - |           5.040 |          60.100 |        3.870998 |          - |


#### Transformasjon ved standard installasjon av Proj

``cs2cs EPSG:7789 EPSG:4936 --area EPSG:1352``

I dette eksemplet initialiseres Proj til å transformere jordsentriske koordinater fra ITRF2014 til EUREF89. Opsjonen "--area" henviser til EPSG-koden på området transformasjonen skal gjelde for. EPSG:1352 som er brukt ovenfor, er koden for "Norway - onshore". Til sammenligning vil tilsvarende transformasjon for Danmark være:

``cs2cs EPSG:7789 EPSG:4936 --area EPSG:1080``

#### Transformasjon fra NN2000-høyder til Sjøkartnull-dybder

Fra og med Proj 9.0.0 er det mulig å transformere sømløst mellom NN2000 og Sjøkartnull

Transformasjon fra NN2000-høyder til Sjøkartnull-dybder:

``cs2cs -d 4 EPSG:4258+EPSG:5941 EPSG:4258+EPSG:9672``

Eller som kortform:

``cs2cs -d 4 EPSG:5942 EPSG:9883``


#### Transformasjon med egendefinerte sammensatte referanserammer

Proj har mulighet til å sette sammen forhåndsdefinerte datum for høyde og grunnriss. For eksempel kan man kombinere ETRS89 med høydedatumet EGM2008. Da kan man 
bruke syntaksen *EPSG:4258+EPSG:3855*.

Utlisting av *EPSG:4258+EPSG:3855* på WKT-format:

``projinfo -k ensemble EPSG:4258+EPSG:3855 -o WKT2:2019``

Transformasjon fra ETRS89 ellipsoidiske høyder til EGM2008:

``cs2cs -d 4 EPSG:4258 EPSG:4258+EPSG:3855``
