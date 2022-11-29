---
layout: default
title: Map Data 
nav_order: 3
parent: Build a Webmap
---

## Map Data
If you haven't already...
{: .label .label-green }
Click on the 'Download Data' button below to start the download. Once complete, **extract the contents of the .zip file**.

Explain what's in it - and alos wehre it calme from 

[Download Data](mapbox-intro.zip){: .btn .btn-blue }

## GeoJSON
The vector layers or map tiles of your interactive basemap provide spatial context for the data you wish spatially visualize. Your data is rendered above your chosen basemap and is called the "data layer", "map content" or sometimes "map features". Usually your data is vector data so you can click and interact with it, but you can also add raster data as well.      

If you’re a GIS user, you have encountered a Shapefile. Shapefiles are the industry standard file type for geographic vector data. If you’ve ever tried to share a Shapefile in the web, you’ve probably had some problems, or needed to transform your file into something else. Shapefiles are meant to be used in GIS software and weren’t designed to be displayed in the web. The [GeoJSON](https://geojson.org/) format on the other hand is a geographic file type specifically meant for the web. They’re “easy for humans to read, and easy for machines to read”, meaning that they’re a lightweight, simplified format so your average web browser can use them, and they’re also fairly easy to understand if you want to view and edit them in a code editor. Here’s a GeoJSON point for one park in Vancouver: 

```json
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [
          -123.108174,
          49.264334
        ]
      },
      "properties": {
        "parkid": 137,
        "official": 1,
        "hectare": 1.4,
        "neighbourhoodname": "Mount Pleasant",
        "facilities": "Y",
        "advisories": "N",
        "name": "Jonathan Rogers Park",
        "ewstreet": "W 7th Avenue",
        "specialfeatures": "N",
        "washrooms": "Y",
        "nsstreet": "Manitoba Street",
        "streetname": "W 7th Avenue",
        "streetnumber": 110,
        "googlemapdest": [
          49.264334,
          -123.108174
        ],
        "neighbourhoodurl": "https://vancouver.ca/news-calendar/mount-pleasant.aspx"
      }
    }
```
Even without prior GeoJSON knowledge, can you deduce the name of this park and whether or not it has washrooms? In contrast, a shapefile is a binary (0s and 1s, not text) format, so you wouldn't be able to read the file with human eyes. For these reasons, we're using GeoJSON files for this workshop.

One other great thing about GeoJSON, is that because they are open-source and simple to understand, there are several tools that allow you to create and edit them in the web, like [geojson.io](http://geojson.io).

To Do
{: .label .label-green }
1. Delete existing geoJSON text on the </>JSON panel of [geojson.io](http://geojson.io).
2. Copy the GeoJSON text above and replace what you just deleted on geojson.io.
3. On the right-hand side of the map interface there is a vertical toolbar. Use the + icon to zoom into Jonathan Rogers Park. Click on the pop-up to see the feature properties. Here you can add new information about the park, for instance, a personal_memory column. Use the edit button (at the bottom of the same toolbar) to drag the point to another location. 







