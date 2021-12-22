---
layout: page
title: OpenAPI transformasjonstjeneste
order: 10
---

Kartverket har utviklet en webtjeneste for transformasjoner. Tjenesten er utviklet i Python og pyproj og byggjer på standarder i OpenAPI-spesifikasjonen. 

## Linker til OpenAPI

* [Link til API'et](https://ws.geonorge.no/transformering/v1/)
* [Link til OpenAPI-skjema](https://ws.geonorge.no/transformering/v1/openapi.json)
* [Link til OpenAPI-spesifikasjonen](https://swagger.io/specification/)		

API'et er også et RESTFul-API (**RE**presentational **S**tate **T**ransfer) med to Get-funksjonar.

* Koordinatsystemer_projeksjoner_get:
> https://ws.geonorge.no/transformering/v1/#/transformering/Koordinatsystemer_projeksjoner_get

* Transformer_transformer_get:
> https://ws.geonorge.no/transformering/v1/#/transformering/Transformer_transformer_get

## Eksempel på bruk av API'et

Ved transformasjon av koordinater med API'et må man, som i Proj generelt, oppgi EPSG-kodene på fra- og til-koordinatsystemene/referanserammene.		

Tilgjengelige EPSG-koder kan hentes ved å legge denne URL'en i en nettleser:

> https://ws.geonorge.no/transformering/v1/projeksjoner

Det vil i praksis være mulig å kunne transformere mellom alle tilgjengelige EPSG-koder som er støtta av API'et.		

Eksempel på transformasjon av koordinaten bredde=65.0 og lengde=12.0 fra EUREF89 geografisk til EUREF89 UTM33:

> https://ws.geonorge.no/transformering/v1/transformer?x=12&y=65&fra=4258&til=25833

<!--
## Testing med net core

* Leggje inn referanse til testklienten.

-->
