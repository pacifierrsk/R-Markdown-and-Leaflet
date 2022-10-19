# R-Markdown-and-Leaflet
Sumary
The Developing Data Products course project uses R Markdown and Leaflet to design a WEB page and an interactive map. In this project, we will use an interactive map of Ciudad Juarez, Mexico’s main points of interest. With this map, users can learn more about this city that borders the United States of America.

Procedure
As a first part, we will define the date of creation of this code
  date()
## [1] "Tue Oct 18 21:04:58 2022"
Loading libraries for Interactive Maps
  library(leaflet)
## Warning: package 'leaflet' was built under R version 4.1.3
  library(dplyr)
## Warning: package 'dplyr' was built under R version 4.1.3
## 
## Attaching package: 'dplyr'
## The following objects are masked from 'package:stats':
## 
##     filter, lag
## The following objects are masked from 'package:base':
## 
##     intersect, setdiff, setequal, union
Locating the points of interest of the City
  m<-leaflet(width = "100%") %>% 
  addTiles() %>% 
  setView(lng= -106.4833300, lat= 31.7333300, zoom = 11) %>% 
  addMarkers(lng= -106.46080455789418, lat= 31.756623020555686, popup= "El Chamizal National Park")%>%
  addMarkers(lng= -106.42353605259582, lat= 31.688145801104024, popup= "Parque Hermanos Escobar")%>%
  addMarkers(lng= -106.46959814247676, lat= 31.739537989368316, popup= "La Casa del Divo de Juarez, Juan Gabriel")%>%
  addMarkers(lng= -106.48313601664597, lat= 31.738434649733684, popup= "Ciudad Juarez DownTown")%>%
  addMarkers(lng= -106.48687567548996, lat= 31.739120897810707, popup= "Catedral del Nuestra Señora de Guadalupe")
  (m)
