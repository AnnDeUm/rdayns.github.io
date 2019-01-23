---
title: "Bureau of Internal Revenue District Offices in the Philippines"
author: "RAD"
date: "January 10, 2019"
output: 
  html_document: 
    keep_md: yes
---

This dataset contains Bureau of Internal Revenue district offices in the Philippines. This data set can be downloaded from: https://data.gov.ph/dataset/revenue-district-offices

##Reading the Data


```r
data <- "https://data.gov.ph/sites/default/files/Revenue%20District%20Office_0.csv"
df <- read.csv(url(data))
```
 

## Plotting Map

```r
library(leaflet)

df %>%
  leaflet() %>%
  addTiles() %>%
  addMarkers(clusterOptions = markerClusterOptions())
```

```
## Assuming "longitude" and "latitude" are longitude and latitude, respectively
```

<!--html_preserve--><div id="htmlwidget-36fcbf09eaf8517a1335" style="width:672px;height:480px;" class="leaflet html-widget"></div>
<script type="application/json" data-for="htmlwidget-36fcbf09eaf8517a1335">{"x":{"options":{"crs":{"crsClass":"L.CRS.EPSG3857","code":null,"proj4def":null,"projectedBounds":null,"options":{}}},"calls":[{"method":"addTiles","args":["//{s}.tile.openstreetmap.org/{z}/{x}/{y}.png",null,null,{"minZoom":0,"maxZoom":18,"tileSize":256,"subdomains":"abc","errorTileUrl":"","tms":false,"noWrap":false,"zoomOffset":0,"zoomReverse":false,"opacity":1,"zIndex":1,"detectRetina":false,"attribution":"&copy; <a href=\"http://openstreetmap.org\">OpenStreetMap<\/a> contributors, <a href=\"http://creativecommons.org/licenses/by-sa/2.0/\">CC-BY-SA<\/a>"}]},{"method":"addMarkers","args":[[18.200054,17.591261,16.592137,15.983475,16.120925,15.968626,17.587403,16.396014,16.44587,17.052271,17.472677,16.807502,17.612166,16.477672,17.124973,16.418536,15.475896,15.667156,14.839267,14.823643,14.674006,15.066869,15.023756,15.733685,15.580641,15.488984,14.694055,14.871562,14.871356,14.658814,14.75671,14.64953,14.590107,14.592296,14.592296,14.592296,14.592296,14.584939,12.41476,9.74025,12.348182,14.649181,14.638083,14.638176,14.574157,14.600955,14.573043,14.559136,14.554925,14.636961,14.55199,14.562035,14.561913,14.560044,14.557251,14.537711,14.475489,14.435165,14.420811,14.279917,14.449265,14.065045,14.216722,14.334689,13.764523,13.962061,13.957667,13.92205,13.448813,13.407227,14.11083,13.624021,13.624031,13.142586,12.980809,13.586361,12.371904,11.708469,11.582384,10.749977,10.69783,10.82257,10.900628,10.901807,10.194493,9.307499,10.320248,10.323852,10.292605,10.266732,9.64472,12.498347,11.603834,11.773461,11.178502,11.00542,10.163534,8.584885,7.824352,6.951961,6.902529,17.019911,8.817571,8.510358,8.153924,8.151391,8.243493,7.997508,8.947125,8.711104,9.791559,9.078384,7.222992,7.008863,6.69209,6.116606,6.476437,7.235862,7.064836,6.951349,6.730379,7.007593],[120.588427,120.455116,120.360835,120.361916,119.992524,120.559157,120.625215,120.592379,120.602835,120.987488,121.466871,121.201072,121.729734,121.147353,121.995652,121.522294,120.59739,120.556408,120.284306,120.283631,120.510337,120.530697,120.688045,121.57142,120.920161,120.967248,120.963964,120.861532,120.862854,120.96388,121.048422,121.028876,120.97088,120.974954,120.974954,120.974954,120.974954,120.994908,121.980668,118.743426,121.065372,121.028756,121.028093,121.028018,121.04383,121.027697,121.061342,121.081632,121.044226,121.098778,121.130359,121.018775,121.018056,121.009559,121.026445,120.994314,121.000966,121.011428,121.043732,120.868502,120.934963,121.288315,121.143783,121.081898,121.061802,121.167474,121.61803,122.09824,121.840083,121.177229,122.955738,123.199653,123.199653,123.750754,124.024813,124.236858,123.622951,122.365964,122.754715,121.941562,122.547898,122.611867,123.072288,123.075037,122.859748,123.294717,123.919602,123.906456,123.880363,123.842572,123.857773,124.640534,125.437603,124.885357,125.002843,124.608387,124.845737,123.342133,123.439203,122.074198,122.080127,121.849629,125.106604,124.623223,125.128435,123.850548,124.252607,124.29356,125.532389,125.74808,125.492806,126.19814,124.247335,125.089885,124.675929,125.170573,124.87231,125.642501,125.598023,126.219787,125.359468,125.097191],null,null,null,{"interactive":true,"draggable":false,"keyboard":true,"title":"","alt":"","zIndexOffset":0,"opacity":1,"riseOnHover":false,"riseOffset":250},null,null,{"showCoverageOnHover":true,"zoomToBoundsOnClick":true,"spiderfyOnMaxZoom":true,"removeOutsideVisibleBounds":true,"spiderLegPolylineOptions":{"weight":1.5,"color":"#222","opacity":0.5},"freezeAtZoom":false},null,null,{"interactive":false,"permanent":false,"direction":"auto","opacity":1,"offset":[0,0],"textsize":"10px","textOnly":false,"className":"","sticky":true},null]}],"limits":{"lat":[6.116606,18.200054],"lng":[118.743426,126.219787]}},"evals":[],"jsHooks":[]}</script><!--/html_preserve-->