---
layout: default
title: Data 
nav_order: 3
parent: Hands On
---

# Map Data
If you haven't already, click on the 'Download Data' button below to start the download. Once complete, **extract the contents of the .zip file**.
    
[Download Data](mapbox-intro.zip){: .btn .btn-blue }

Inside the workshop data folder you will see the boilerplate.html file we looked at earlier, as well as `van-parks.geojson`, a geospatial file downloaded from Vancouver's [open data portal](https://opendata.vancouver.ca/explore/dataset/parks/map/?location=14,49.2717,-123.12271).  `van-parks.geojson` contains points for 216 parks across the city. Take a moment to view the dataset as a table and map in th open data portal. 

## GeoJSON      

If you’ve used a geographic information system (GIS) before then you have likely encountered a Shapefile. Shapefiles are the industry standard file type for geographic vector data. Shapefiles are meant to be used in GIS software and weren’t designed to be displayed in the web. The [GeoJSON](https://geojson.org/) format, on the other hand, is a geographic file type specifically meant for the web. GeoJSON files are “easy for humans to read, and easy for machines to read”, meaning that they’re a lightweight, simplified format so your average web browser can use them. GeoJSON code is fairly straightforward making it easy to understand and modify properties in a code editor. Here’s a single point for a park in Vancouver in GeoJSON format: 

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
Even without prior GeoJSON knowledge, can you deduce the name of this park and whether or not it has washrooms? A shapefile, in contrast, is a binary (0s and 1s, not text) format, so you wouldn't be able to read the file with human eyes.For these reasons, this workshop uses GeoJSON data. 


To Do
{: .label .label-green }

One other great thing about GeoJSON, is that because they are open-source and simple to understand, there are several tools that allow you to create and edit them in the web, like [geojson.io](http://geojson.io).


1. Go to [geojson.io](http://geojson.io) and delete existing geoJSON text on the </>JSON panel.
2. Copy the GeoJSON text above and paste it into the blank the </>JSON panel. 
3. On the right-hand side of the map interface there is a vertical toolbar.Use the + icon from the map toolbar to zoom into the icon that for Jonathan Rogers Park you just added to the basemap.  Click on the pop-up to see the feature properties. Here you can add new information about the park, for instance, a personal_memory column. Use the edit button (at the bottom of the same toolbar) to drag the point to another location. 
4. Open [geojson.io](http://geojson.io) again in a new tab. Drag and drop `van-parks.geojson` into the </>JSON panel. This is a quick and easy way to visualize a GeoJSON dataset before you begin web-mapping. Now let's return to the code editor and add `van-parks.geojson` to the map.  


![Workshop Data in geojson.io](./images/workshop-data-geojsonio_20221127.png)






