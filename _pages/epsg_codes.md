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

| EPSG-kode | Namn | Type | EPSG - base crs | Evt. gamal EPSG-kode | Merknad |
| --- | --- | --- | --- | --- | --- |
| 1407 | ETRS89-NOR [EUREF89] | geodetic (datum) |  | 6258 |  |
| 10873 | ETRS89-NOR [EUREF89] | geocentric | 1407 | 4936 |  |
| 10874 | ETRS89-NOR [EUREF89] | geographic 3D | 1407 | 4937 |  |
| 10875 | ETRS89-NOR [EUREF89] | geographic 2D | 1407 | 4258 |  |
| 11394 | NN2000:2025 height | Vertical crs |  |  |  |
| 11399 | ETRS89-NOR [EUREF89] + NN2000:2025 height | Compound crs | 10874 + 11394 |  | Ny kode |
| 5941 | NN2000:2018 height | Vertical crs |  |  | Nytt namn |
| 11558 | ETRS89-NOR [EUREF89] + NN2000:2018 height | Compound crs | 10875 + 5941 | 5942 | Nytt namn |
| 11560 | ETRS89-NOR [EUREF89] + NN54 height | Compound crs | 10875 + 5776 | 6144 | Nytt namn |
| 11565 | ETRS89-NOR [EUREF89] + CD Norway depth | Compound crs | 10875 + 9672 | 9883 | Nytt namn |
| 10999 | SVD2024 height | Vertical crs |  | - |  |
| 11000 | ETRS89-NOR [EUREF89] + SVD2024 height | Compound crs | 10875 + 10999 |  | Ny kode |
| 11563 | ETRS89-NOR [EUREF89] + SVD2006 height | Compound crs | 10875 + 20000 | 20001 |  |
| 5105 | ETRS89-NOR [EUREF89] / NTM zone 5 | Projected crs | 10875 | 4855 |  |
| 5106 | ETRS89-NOR [EUREF89] / NTM zone 6 | Projected crs | 10875 | 4856 |  |
| 5107 | ETRS89-NOR [EUREF89] / NTM zone 7 | Projected crs | 10875 | 4857 |  |
| 5108 | ETRS89-NOR [EUREF89] / NTM zone 8 | Projected crs | 10875 | 4858 |  |
| 5109 | ETRS89-NOR [EUREF89] / NTM zone 9 | Projected crs | 10875 | 4859 |  |
| 5110 | ETRS89-NOR [EUREF89] / NTM zone 10 | Projected crs | 10875 | 4860 |  |
| 5111 | ETRS89-NOR [EUREF89] / NTM zone 11 | Projected crs | 10875 | 4861 |  |
| 5112 | ETRS89-NOR [EUREF89] / NTM zone 12 | Projected crs | 10875 | 4862 |  |
| 5113 | ETRS89-NOR [EUREF89] / NTM zone 13 | Projected crs | 10875 | 4863 |  |
| 5114 | ETRS89-NOR [EUREF89] / NTM zone 14 | Projected crs | 10875 | 4864 |  |
| 5115 | ETRS89-NOR [EUREF89] / NTM zone 15 | Projected crs | 10875 | 4865 |  |
| 5116 | ETRS89-NOR [EUREF89] / NTM zone 16 | Projected crs | 10875 | 4866 |  |
| 5117 | ETRS89-NOR [EUREF89] / NTM zone 17 | Projected crs | 10875 | 4867 |  |
| 5118 | ETRS89-NOR [EUREF89] / NTM zone 18 | Projected crs | 10875 | 4868 |  |
| 5119 | ETRS89-NOR [EUREF89] / NTM zone 19 | Projected crs | 10875 | 4869 |  |
| 5120 | ETRS89-NOR [EUREF89] / NTM zone 20 | Projected crs | 10875 | 4870 |  |
| 5121 | ETRS89-NOR [EUREF89] / NTM zone 21 | Projected crs | 10875 | 4871 |  |
| 5122 | ETRS89-NOR [EUREF89] / NTM zone 22 | Projected crs | 10875 | 4872 |  |
| 5123 | ETRS89-NOR [EUREF89] / NTM zone 23 | Projected crs | 10875 | 4873 |  |
| 5124 | ETRS89-NOR [EUREF89] / NTM zone 24 | Projected crs | 10875 | 4874 |  |
| 5125 | ETRS89-NOR [EUREF89] / NTM zone 25 | Projected crs | 10875 | 4875 |  |
| 5126 | ETRS89-NOR [EUREF89] / NTM zone 26 | Projected crs | 10875 | 4876 |  |
| 5127 | ETRS89-NOR [EUREF89] / NTM zone 27 | Projected crs | 10875 | 4877 |  |
| 5128 | ETRS89-NOR [EUREF89] / NTM zone 28 | Projected crs | 10875 | 4878 |  |
| 5129 | ETRS89-NOR [EUREF89] / NTM zone 29 | Projected crs | 10875 | 4879 |  |
| 5130 | ETRS89-NOR [EUREF89] / NTM zone 30 | Projected crs | 10875 | 4880 |  |
| 5945 | ETRS89-NOR [EUREF89] / NTM zone 5 + NN2000:2018 height | Compound crs | 5105 + 5941 |  |  |
| 5946 | ETRS89-NOR [EUREF89] / NTM zone 6 + NN2000:2018 height | Compound crs | 5106 + 5941 |  |  |
| 5947 | ETRS89-NOR [EUREF89] / NTM zone 7 + NN2000:2018 height | Compound crs | 5107 + 5941 |  |  |
| 5948 | ETRS89-NOR [EUREF89] / NTM zone 8 + NN2000:2018 height | Compound crs | 5108 + 5941 |  |  |
| 5949 | ETRS89-NOR [EUREF89] / NTM zone 9 + NN2000:2018 height | Compound crs | 5109 + 5941 |  |  |
| 5950 | ETRS89-NOR [EUREF89] / NTM zone 10 + NN2000:2018 height | Compound crs | 5110 + 5941 |  |  |
| 5951 | ETRS89-NOR [EUREF89] / NTM zone 11 + NN2000:2018 height | Compound crs | 5111 + 5941 |  |  |
| 5952 | ETRS89-NOR [EUREF89] / NTM zone 12 + NN2000:2018 height | Compound crs | 5112 + 5941 |  |  |
| 5953 | ETRS89-NOR [EUREF89] / NTM zone 13 + NN2000:2018 height | Compound crs | 5113 + 5941 |  |  |
| 5954 | ETRS89-NOR [EUREF89] / NTM zone 14 + NN2000:2018 height | Compound crs | 5114 + 5941 |  |  |
| 5955 | ETRS89-NOR [EUREF89] / NTM zone 15 + NN2000:2018 height | Compound crs | 5115 + 5941 |  |  |
| 5956 | ETRS89-NOR [EUREF89] / NTM zone 16 + NN2000:2018 height | Compound crs | 5116 + 5941 |  |  |
| 5957 | ETRS89-NOR [EUREF89] / NTM zone 17 + NN2000:2018 height | Compound crs | 5117 + 5941 |  |  |
| 5958 | ETRS89-NOR [EUREF89] / NTM zone 18 + NN2000:2018 height | Compound crs | 5111 + 5941 |  |  |
| 5959 | ETRS89-NOR [EUREF89] / NTM zone 19 + NN2000:2018 height | Compound crs | 5119 + 5941 |  |  |
| 5960 | ETRS89-NOR [EUREF89] / NTM zone 20 + NN2000:2018 height | Compound crs | 5120 + 5941 |  |  |
| 5961 | ETRS89-NOR [EUREF89] / NTM zone 21 + NN2000:2018 height | Compound crs | 5121 + 5941 |  |  |
| 5962 | ETRS89-NOR [EUREF89] / NTM zone 22 + NN2000:2018 height | Compound crs | 5122 + 5941 |  |  |
| 5963 | ETRS89-NOR [EUREF89] / NTM zone 23 + NN2000:2018 height | Compound crs | 5123 + 5941 |  |  |
| 5964 | ETRS89-NOR [EUREF89] / NTM zone 24 + NN2000:2018 height | Compound crs | 5124 + 5941 |  |  |
| 5965 | ETRS89-NOR [EUREF89] / NTM zone 25 + NN2000:2018 height | Compound crs | 5125 + 5941 |  |  |
| 5966 | ETRS89-NOR [EUREF89] / NTM zone 26 + NN2000:2018 height | Compound crs | 5126 + 5941 |  |  |
| 5967 | ETRS89-NOR [EUREF89] / NTM zone 27 + NN2000:2018 height | Compound crs | 5127 + 5941 |  |  |
| 5968 | ETRS89-NOR [EUREF89] / NTM zone 28 + NN2000:2018 height | Compound crs | 5128 + 5941 |  |  |
| 5969 | ETRS89-NOR [EUREF89] / NTM zone 29 + NN2000:2018 height | Compound crs | 5129 + 5941 |  |  |
| 5970 | ETRS89-NOR [EUREF89] / NTM zone 30 + NN2000:2018 height | Compound crs | 5130 + 5941 |  |  |
| 5971 | ETRS89-NOR [EUREF89] / UTM zone 31N + NN2000:2018 height | Compound crs | 11021 + 5941 | 5971 | Endra 2D-system |
| 5972 | ETRS89-NOR [EUREF89] / UTM zone 32N + NN2000:2018 height | Compound crs | 11022 + 5941 | 5972 | Endra 2D-system |
| 5973 | ETRS89-NOR [EUREF89] / UTM zone 33N + NN2000:2018 height | Compound crs | 11023 + 5941 | 5973 | Endra 2D-system |
| 5974 | ETRS89-NOR [EUREF89] / UTM zone 34N + NN2000:2018 height | Compound crs | 11024 + 5941 | 5974 | Endra 2D-system |
| 5975 | ETRS89-NOR [EUREF89] / UTM zone 35N + NN2000:2018 height | Compound crs | 11025 + 5941 | 5975 | Endra 2D-system |
| 5976 | ETRS89-NOR [EUREF89] / UTM zone 36N + NN2000:2018 height | Compound crs | 11026 + 5941 | 5976 | Endra 2D-system |
| 6145 | ETRS89-NOR [EUREF89] / NTM zone 5 + NN54 height | Compound crs | 5105 + 5776 |  |  |
| 6146 | ETRS89-NOR [EUREF89] / NTM zone 6 + NN54 height | Compound crs | 5106 + 5776 |  |  |
| 6147 | ETRS89-NOR [EUREF89] / NTM zone 7 + NN54 height | Compound crs | 5107 + 5776 |  |  |
| 6148 | ETRS89-NOR [EUREF89] / NTM zone 8 + NN54 height | Compound crs | 5108 + 5776 |  |  |
| 6149 | ETRS89-NOR [EUREF89] / NTM zone 9 + NN54 height | Compound crs | 5109 + 5776 |  |  |
| 6150 | ETRS89-NOR [EUREF89] / NTM zone 10 + NN54 height | Compound crs | 5110 + 5776 |  |  |
| 6151 | ETRS89-NOR [EUREF89] / NTM zone 11 + NN54 height | Compound crs | 5111 + 5776 |  |  |
| 6152 | ETRS89-NOR [EUREF89] / NTM zone 12 + NN54 height | Compound crs | 5112 + 5776 |  |  |
| 6153 | ETRS89-NOR [EUREF89] / NTM zone 13 + NN54 height | Compound crs | 5113 + 5776 |  |  |
| 6154 | ETRS89-NOR [EUREF89] / NTM zone 14 + NN54 height | Compound crs | 5114 + 5776 |  |  |
| 6155 | ETRS89-NOR [EUREF89] / NTM zone 15 + NN54 height | Compound crs | 5115 + 5776 |  |  |
| 6156 | ETRS89-NOR [EUREF89] / NTM zone 16 + NN54 height | Compound crs | 5116 + 5776 |  |  |
| 6157 | ETRS89-NOR [EUREF89] / NTM zone 17 + NN54 height | Compound crs | 5117 + 5776 |  |  |
| 6158 | ETRS89-NOR [EUREF89] / NTM zone 18 + NN54 height | Compound crs | 5118 + 5776 |  |  |
| 6159 | ETRS89-NOR [EUREF89] / NTM zone 19 + NN54 height | Compound crs | 5119 + 5776 |  |  |
| 6160 | ETRS89-NOR [EUREF89] / NTM zone 20 + NN54 height | Compound crs | 5120 + 5776 |  |  |
| 6161 | ETRS89-NOR [EUREF89] / NTM zone 21 + NN54 height | Compound crs | 5121 + 5776 |  |  |
| 6162 | ETRS89-NOR [EUREF89] / NTM zone 22 + NN54 height | Compound crs | 5122 + 5776 |  |  |
| 6163 | ETRS89-NOR [EUREF89] / NTM zone 23 + NN54 height | Compound crs | 5123 + 5776 |  |  |
| 6164 | ETRS89-NOR [EUREF89] / NTM zone 24 + NN54 height | Compound crs | 5124 + 5776 |  |  |
| 6165 | ETRS89-NOR [EUREF89] / NTM zone 25 + NN54 height | Compound crs | 5125 + 5776 |  |  |
| 6166 | ETRS89-NOR [EUREF89] / NTM zone 26 + NN54 height | Compound crs | 5126 + 5776 |  |  |
| 6167 | ETRS89-NOR [EUREF89] / NTM zone 27 + NN54 height | Compound crs | 5127 + 5776 |  |  |
| 6168 | ETRS89-NOR [EUREF89] / NTM zone 28 + NN54 height | Compound crs | 5128 + 5776 |  |  |
| 6169 | ETRS89-NOR [EUREF89] / NTM zone 29 + NN54 height | Compound crs | 5129 + 5776 |  |  |
| 6170 | ETRS89-NOR [EUREF89] / NTM zone 30 + NN54 height | Compound crs | 5130 + 5776 |  |  |
| 6171 | ETRS89-NOR [EUREF89] / UTM zone 31N + NN54 height | Compound crs | 11021 + 5776 | 6171 | Endra 2D-system |
| 6172 | ETRS89-NOR [EUREF89] / UTM zone 32N + NN54 height | Compound crs | 11022 + 5776 | 6172 | Endra 2D-system |
| 6173 | ETRS89-NOR [EUREF89] / UTM zone 33N + NN54 height | Compound crs | 11023 + 5776 | 6173 | Endra 2D-system |
| 6174 | ETRS89-NOR [EUREF89] / UTM zone 34N + NN54 height | Compound crs | 11024 + 5776 | 6174 | Endra 2D-system |
| 6175 | ETRS89-NOR [EUREF89] / UTM zone 35N + NN54 height | Compound crs | 11025 + 5776 | 6175 | Endra 2D-system |
| 6176 | ETRS89-NOR [EUREF89] / UTM zone 36N + NN54 height | Compound crs | 11026 + 5776 | 6176 | Endra 2D-system |
| 11012 | ETRS89-NOR [EUREF89] / UTM zone 30N (N-E) | Projected crs | 10875 | 3042 |  |
| 11013 | ETRS89-NOR [EUREF89] / UTM zone 31N (N-E) | Projected crs | 10875 | 3043 |  |
| 11014 | ETRS89-NOR [EUREF89] / UTM zone 32N (N-E) | Projected crs | 10875 | 3044 |  |
| 11015 | ETRS89-NOR [EUREF89] / UTM zone 33N (N-E) | Projected crs | 10875 | 3045 |  |
| 11016 | ETRS89-NOR [EUREF89] / UTM zone 34N (N-E) | Projected crs | 10875 | 3046 |  |
| 11017 | ETRS89-NOR [EUREF89] / UTM zone 35N (N-E) | Projected crs | 10875 | 3047 |  |
| 11018 | ETRS89-NOR [EUREF89] / UTM zone 36N (N-E) | Projected crs | 10875 | 3048 |  |
| 11019 | ETRS89-NOR [EUREF89] / UTM zone 37N (N-E) | Projected crs | 10875 | 3049 |  |
| 11020 | ETRS89-NOR [EUREF89] / UTM zone 30N | Projected crs | 10875 | 25830 |  |
| 11021 | ETRS89-NOR [EUREF89] / UTM zone 31N | Projected crs | 10875 | 25831 |  |
| 11022 | ETRS89-NOR [EUREF89] / UTM zone 32N | Projected crs | 10875 | 25832 |  |
| 11023 | ETRS89-NOR [EUREF89] / UTM zone 33N | Projected crs | 10875 | 25833 |  |
| 11024 | ETRS89-NOR [EUREF89] / UTM zone 34N | Projected crs | 10875 | 25834 |  |
| 11025 | ETRS89-NOR [EUREF89] / UTM zone 35N | Projected crs | 10875 | 25835 |  |
| 11026 | ETRS89-NOR [EUREF89] / UTM zone 36N | Projected crs | 10875 | 25836 |  |
| 11027 | ETRS89-NOR [EUREF89] / UTM zone 37N | Projected crs | 10875 | 25837 |  |
| 11400 | ETRS89-NOR [EUREF89] / UTM zone 31N + NN2000:2025 height | Compound crs | 11021 + 11394 |  | Ny kode |
| 11403 | ETRS89-NOR [EUREF89] / UTM zone 32N + NN2000:2025 height | Compound crs | 11022 + 11394 |  | Ny kode |
| 11404 | ETRS89-NOR [EUREF89] / UTM zone 33N + NN2000:2025 height | Compound crs | 11023 + 11394 |  | Ny kode |
| 11405 | ETRS89-NOR [EUREF89] / UTM zone 34N + NN2000:2025 height | Compound crs | 11024 + 11394 |  | Ny kode |
| 11406 | ETRS89-NOR [EUREF89] / UTM zone 35N + NN2000:2025 height | Compound crs | 11025 + 11394 |  | Ny kode |
| 11407 | ETRS89-NOR [EUREF89] / UTM zone 36N + NN2000:2025 height | Compound crs | 11026 + 11394 |  | Ny kode |
| 11408 | ETRS89-NOR [EUREF89] / NTM zone 8 + NN2000:2025 height | Compound crs | 5108 + 11394 |  | Ny kode |
| 11409 | ETRS89-NOR [EUREF89] / NTM zone 9 + NN2000:2025 height | Compound crs | 5109 + 11394 |  | Ny kode |
| 11410 | ETRS89-NOR [EUREF89] / NTM zone 10 + NN2000:2025 height | Compound crs | 5110 + 11394 |  | Ny kode |
| 11411 | ETRS89-NOR [EUREF89] / NTM zone 11 + NN2000:2025 height | Compound crs | 5111 + 11394 |  | Ny kode |
| 11412 | ETRS89-NOR [EUREF89] / NTM zone 12 + NN2000:2025 height | Compound crs | 5112 + 11394 |  | Ny kode |
| 11413 | ETRS89-NOR [EUREF89] / NTM zone 13 + NN2000:2025 height | Compound crs | 5113 + 11394 |  | Ny kode |
| 11414 | ETRS89-NOR [EUREF89] / NTM zone 14 + NN2000:2025 height | Compound crs | 5114 + 11394 |  | Ny kode |
| 11415 | ETRS89-NOR [EUREF89] / NTM zone 15 + NN2000:2025 height | Compound crs | 5115 + 11394 |  | Ny kode |
| 11416 | ETRS89-NOR [EUREF89] / NTM zone 16 + NN2000:2025 height | Compound crs | 5116 + 11394 |  | Ny kode |
| 11417 | ETRS89-NOR [EUREF89] / NTM zone 17 + NN2000:2025 height | Compound crs | 5117 + 11394 |  | Ny kode |
| 11418 | ETRS89-NOR [EUREF89] / NTM zone 18 + NN2000:2025 height | Compound crs | 5118 + 11394 |  | Ny kode |
| 11419 | ETRS89-NOR [EUREF89] / NTM zone 19 + NN2000:2025 height | Compound crs | 5119 + 11394 |  | Ny kode |
| 11420 | ETRS89-NOR [EUREF89] / NTM zone 20 + NN2000:2025 height | Compound crs | 5120 + 11394 |  | Ny kode |
| 11421 | ETRS89-NOR [EUREF89] / NTM zone 21 + NN2000:2025 height | Compound crs | 5121 + 11394 |  | Ny kode |
| 11422 | ETRS89-NOR [EUREF89] / NTM zone 22 + NN2000:2025 height | Compound crs | 5122 + 11394 |  | Ny kode |
| 11423 | ETRS89-NOR [EUREF89] / NTM zone 23 + NN2000:2025 height | Compound crs | 5123 + 11394 |  | Ny kode |
| 11424 | ETRS89-NOR [EUREF89] / NTM zone 24 + NN2000:2025 height | Compound crs | 5124 + 11394 |  | Ny kode |
| 11425 | ETRS89-NOR [EUREF89] / NTM zone 25 + NN2000:2025 height | Compound crs | 5125 + 11394 |  | Ny kode |
| 11426 | ETRS89-NOR [EUREF89] / NTM zone 26 + NN2000:2025 height | Compound crs | 5126 + 11394 |  | Ny kode |
| 11427 | ETRS89-NOR [EUREF89] / NTM zone 27 + NN2000:2025 height | Compound crs | 5127 + 11394 |  | Ny kode |
| 11428 | ETRS89-NOR [EUREF89] / NTM zone 28 + NN2000:2025 height | Compound crs | 5128 + 11394 |  | Ny kode |
| 11429 | ETRS89-NOR [EUREF89] / NTM zone 29 + NN2000:2025 height | Compound crs | 5129 + 11394 | : | Ny kode |
| 11430 | ETRS89-NOR [EUREF89] / NTM zone 30 + NN2000:2025 height | Compound crs | 5130 + 11394 |  | Ny kode |
| 11435 | ETRS89-NOR [EUREF89] / NTM zone 5 + NN2000:2025 height | Compound crs | 5105 + 11394 |  | Ny kode |
| 11436 | ETRS89-NOR [EUREF89] / NTM zone 6 + NN2000:2025 height | Compound crs | 5106 + 11394 |  | Ny kode |
| 11437 | ETRS89-NOR [EUREF89] / NTM zone 7 + NN2000:2025 height | Compound crs | 5107 + 11394 |  | Ny kode |


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
|  EPSG:9988 |  EPSG:4936 |  1874722.01378 |  912943.23060 |  6007499.79547 |  2020.00 |  1874722.628558 |   912942.991261 |  6007499.590482 |          - |
|  EPSG:4937 |  EPSG:4273 |         10.000 |        60.000 |              - |        - | 10.004772119609 | 59.999247563843 |               - |          - |
| EPSG:25832 | EPSG:27393 |     500000.000 |   6600000.000 |              - |        - |     -97197.1595 |     172511.9003 |               - |          - |
|  EPSG:4230 |  EPSG:4326 |         10.000 |        60.000 |              - |        - |  9.998594123185 | 59.999544266822 |               - |          - |
|  EPSG:4230 |  EPSG:4326 |          3.000 |        60.000 |              - |        - |  2.998327769141 | 59.999460761204 |               - |          - |
|  EPSG:4258 |  EPSG:5941 |         12.000 |        60.000 |        100.000 |        - |          12.000 |          60.000 |       64.266998 |          - |
|  EPSG:4937 |  EPSG:5776 |         12.000 |        60.000 |        100.000 |        - |          12.000 |          60.000 |       64.054001 |          - |
| EPSG:25832 |  EPSG:5972 |     500000.000 |   6600000.000 |        100.000 |        - |      500000.000 |     6600000.000 |       58.042431 |          - |
| EPSG:25832 |  EPSG:6172 |     500000.000 |   6600000.000 |        100.000 |        - |      500000.000 |     6600000.000 |       58.039824 |          - |
|  EPSG:4258 |  EPSG:4230 |         13.000 |        65.000 |              - |        - | 13.001511386767 | 65.000212324075 |               - |          - |
|  EPSG:7912 |  EPSG:4937 |         10.000 |        60.000 |        100.000 |  2020.00 |  9.999991896247 | 59.999995111756 |       99.866516 |          - |
|  EPSG:7912 |  EPSG:4937 |         10.000 |        60.000 |        100.000 |  2010.00 |  9.999994703625 | 59.999996480391 |       99.913775 |          - |
|  EPSG:4937 |  EPSG:9883 |          5.040 |        60.100 |         40.000 |        - |           5.040 |          60.100 |        3.870998 |          - |
|  EPSG:4937 | EPSG:20001 |         15.000 |        78.000 |        100.000 |        - |          15.000 |          78.000 |       67.910250 |          - |

### Transformasjon ved standard installasjon av Proj

``cs2cs EPSG:7789 EPSG:4936 --area EPSG:1352``

I dette eksemplet initialiseres Proj til å transformere jordsentriske koordinater fra ITRF2014 til EUREF89. Opsjonen "--area" henviser til EPSG-koden på området transformasjonen skal gjelde for. EPSG:1352 som er brukt ovenfor, er koden for "Norway - onshore". Til sammenligning vil tilsvarende transformasjon for Danmark være:

``cs2cs EPSG:7789 EPSG:4936 --area EPSG:1080``

### Transformasjon med *--3d*-option (nytt i Proj v. 9.1.0)

Hvis koordinatsystemet som man transformerer fra er horisontal (2D) må man legge til optionen *--3d*.

Feil:
```
cs2cs -d 4 EPSG:4258 EPSG:4258+EPSG:5941
60 10 100
60.0000 10.0000 100.0000
```

Riktig:
```
cs2cs -d 4 --3d EPSG:4258 EPSG:4258+EPSG:5941
60 10 100
60.0000 10.0000 59.4360
```

### Transformasjon fra NN2000-høyder til Sjøkartnull-dybder

Fra og med Proj 9.0.0 er det mulig å transformere sømløst mellom NN2000 og Sjøkartnull

Transformasjon fra NN2000-høyder til Sjøkartnull-dybder:

``cs2cs -d 4 EPSG:4258+EPSG:5941 EPSG:4258+EPSG:9672``

Eller som kortform:

``cs2cs -d 4 EPSG:5942 EPSG:9883``


### Transformasjon med egendefinerte sammensatte referanserammer

Proj har mulighet til å sette sammen forhåndsdefinerte datum for høyde og grunnriss. For eksempel kan man kombinere ETRS89 med høydedatumet EGM2008. Da kan man 
bruke syntaksen *EPSG:4258+EPSG:3855*.

Utlisting av *EPSG:4258+EPSG:3855* på WKT-format:

``projinfo -k ensemble EPSG:4258+EPSG:3855 -o WKT2:2019``

Transformasjon fra ETRS89 ellipsoidiske høyder til EGM2008:

``cs2cs -d 4 EPSG:4937 EPSG:4258+EPSG:3855``


### Transformasjon fra og til fil med *cs2cs*-kommandoen

``cs2cs -d <desimaler> EPSG:<fra-kode> EPSG:<til-kode> <path fra-fil> > <path til-fil>``

Eksempel transformasjon fra *ETRS89 3D geogr.* til *ETRS89 UTM 32 NN2000*:

``cs2cs -d 4 EPSG:4937 EPSG:25832+EPSG:5941 innfil.txt > utfil.txt``

Formatet på *innfil.txt* kan være:

```
60.1441561 10.2520844 116.5761 Hønefoss1
60.1432313 10.2590881 117.1235 Hønefoss2
60.1430092 10.2587710 115.0488 Hønefoss3
```
