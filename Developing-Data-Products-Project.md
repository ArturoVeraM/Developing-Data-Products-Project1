---
title: "Ten tourist places in Azcapotzalco, CDMX"
author: "Arturo Vera"
date: "3/28/2021"
output: 
  html_document:
    keep_md: true
---

## R Markdown and Leaflet

Create a web page using R Markdown that features a map created with Leaflet. 

Host your webpage on either GitHub Pages, RPubs, or NeoCities.

Your webpage must contain the date that you created the document, and it must contain a map created with Leaflet. We would love to see you show off your creativity!


```r
library(leaflet)

places <- data.frame(
  nam = c("Parque Tezozomoc","Casa de Toño","Dux de Venecia","Restaurante Nicos","Mercado de Azcapotzalco",
           "Casa de la Cultura de Azcapotzalco","Cafeteria el Nevado","Alameda Norte","Parque de la China",
           "Catedral de los Santos Apóstoles Felipe y Santiago"),
  lat = c(19.50101524,19.46672967,19.48012694,19.46527708,19.48309872,19.48083034,19.48021267,19.50009348,
           19.46504255,19.48078335),
  lng = c(-99.21051619,-99.1864511,-99.18674996,-99.17775963,-99.18550199,-99.18631552,-99.18651999,-99.17851397,
           -99.17864086,-99.18523568))

places %>% leaflet() %>% addTiles() %>% addCircles(weight = 10, radius = 10, popup = places$nam)
```

<!--html_preserve--><div id="htmlwidget-839a1272b7d5a09e0b1b" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-839a1272b7d5a09e0b1b">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addCircles","args":[[19.50101524,19.46672967,19.48012694,19.46527708,19.48309872,19.48083034,19.48021267,19.50009348,19.46504255,19.48078335],[-99.21051619,-99.1864511,-99.18674996,-99.17775963,-99.18550199,-99.18631552,-99.18651999,-99.17851397,-99.17864086,-99.18523568],10,null,null,{"interactive":true,"className":"","stroke":true,"color":"#03F","weight":10,"opacity":0.5,"fill":true,"fillColor":"#03F","fillOpacity":0.2},["Parque Tezozomoc","Casa de Toño","Dux de Venecia","Restaurante Nicos","Mercado de Azcapotzalco","Casa de la Cultura de Azcapotzalco","Cafeteria el Nevado","Alameda Norte","Parque de la China","Catedral de los Santos Apóstoles Felipe y Santiago"],null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null,null]}],"limits":{"lat":[19.46504255,19.50101524],"lng":[-99.21051619,-99.17775963]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->
