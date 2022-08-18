---
layout: page
title: OpenAPI transformasjonstjeneste
order: 11
---

Kartverket har utviklet en tjeneste for transformasjoner. Tjenesten er utviklet i Python og pyproj og byggjer på standarder i OpenAPI-spesifikasjonen. 

## Linker til OpenAPI

* [Link til API'et](https://ws.geonorge.no/transformering/v1/)
* [Link til OpenAPI-skjema](https://ws.geonorge.no/transformering/v1/openapi.json)
* [Link til OpenAPI-spesifikasjonen](https://swagger.io/specification/)		

API'et er også et RESTFul-API (**RE**presentational **S**tate **T**ransfer) med to GET-requests og en POST-request:

* *Koordinatsystemer_projeksjoner_get* - Retur av tilgjenglige EPSG-koder
> https://ws.geonorge.no/transformering/v1/#/transformering/Koordinatsystemer_projeksjoner_get

* *Transformer_transformer_get* - Retur av transformert enkeltpunkt
> https://ws.geonorge.no/transformering/v1/#/transformering/Transformer_transformer_get

* *Transformer_mange_koordinater_transformer_post* - Retur av flere transformerte koordinater
> https://ws.geonorge.no/transformering/v1/#/transformering/Transformer_mange_koordinater_transformer_post


## Eksempel på bruk av API'et

Ved transformasjon av koordinater med API'et må man, som i Proj generelt, oppgi EPSG-kodene på fra- og til-koordinatsystemene/referanserammene.		

Tilgjengelige EPSG-koder kan hentes ved å legge denne URL'en i en nettleser:

> https://ws.geonorge.no/transformering/v1/projeksjoner

Det vil i praksis være mulig å kunne transformere mellom alle tilgjengelige EPSG-koder som er støtta av API'et.		

Eksempel på transformasjon av koordinaten bredde=65.0 og lengde=12.0 fra 2D EUREF89 geografisk til EUREF89 UTM33:

> https://ws.geonorge.no/transformering/v1/transformer?x=12&y=65&fra=4258&til=25833

Eksempel på massetransformasjon:

Massetransformasjon kjøres som en POST-request med URL'en:

> https://ws.geonorge.no/transformering/v1/transformer?fra=4937&til=25832

URL'en spesifiserer at man skal transformere fra 3D EUREF89 geografisk til EUREF89 UTM32.		

Strømmen med koordinater legges inn som *Request body* på følgende format:

 > [{"x":10.0,"y":60.0,"z":100.1},{"x":10.0,"y":61.1},{"x":10.4,"y":62.5}]

I strømmen av koordinater tilsvarer *x* lengdegrad, *y* breddegrad og *z* høyde. Et punkt kan oppgis som både 2D ( *{"x": ,"y": }* ) og 3D ( *{"x": ,"y": , "z": }* ) ved denne transformasjonen.


<!--
## Testing med net core

* Leggje inn referanse til testklienten.

-->
