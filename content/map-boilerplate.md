---
layout: default
title: Boilerplate Code
nav_order: 1
parent: Hands On
---

# Boilerplate

A boilerplate code is a chunk of code that can be used as-is in multiple contexts and often provides the basis for more advanced operations. The boilerplate code for this workshop renders a basemap which we will tinker with and add to in order to build an dynamic cluster map.

## Boilerplate Basemap

Let's first see what the boilerplate basemap looks like. Unzip and open the `mapbox-intro` data folder that you downloaded for this workshop. Locate the file `boilerplate.html` and right-click to open with VS Code (or your preferred code editor). 

On line 12, replace `PASTE_YOUR_ACCESS_TOKEN_HERE` with your Mapbox Access Token generated earlier. Then, save your HTML file and open it in your web browser. You may need to right-click the file in your folder and open it with your browser of choice. You should see an interactive basemap centered on Vancouver. Use the controls to zoom in and out and pan around your web map. At the bottom of the map frame you'll see that this web map is powered by Mapbox, and uses geospatial data from OpenStreetMap.

Alternatively, if you installed the Live Server extension to Visual Studio Code, in the blue ribbon at the bottom of your code editor there should be an option to "Go Live." Click "Go Live" to open the boilerplate basemap in a web browser.

Keep this browser tab open - we'll return to it in the next section.

## Boilerplate Code

Now let's look at the code powering this map. Return to the `boilerplate.html` file open in your code editor. You should see the code below, code that is responsible for rendering the basemap. (Your boilerplate will also have //comments beneath the code which merely provide scaffolding for what we'll add later.)

```html
<html>
  <head>
    <title>Boilerplate Code</title>
    <link href="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.css" rel="stylesheet">
    <script src="https://api.mapbox.com/mapbox-gl-js/v2.15.0/mapbox-gl.js"></script>
  </head>

  <body>
    <div id="map" style="width: 700px; height: 600px; margin: auto;"></div>
    <script>
      mapboxgl.accessToken = "YOUR_ACCESS_TOKEN";
      const map = new mapboxgl.Map({
        container: "map",
        style: "mapbox://styles/mapbox/streets-v12",
        center: [-123.11738086752482, 49.25090077610571],
        zoom: 10,
        projection: "globe",
      });
      map.addControl(new mapboxgl.NavigationControl());
    </script>
  </body>
</html>
```


## Anatomy of an HTML document 
The HTML document is split into two main sections: the <code>head</code> and the <code>body</code>. Each of these sections are contained within opening < tags > and closing </ tags >. Notice that because the document is in HTML format, everything is contained within the html tag.

```html
<html>
  <head>
    The stuff inside the head is the metadata for your browser about the
    document. Inside the head are things like the document’s title - in this
    case “Boilerplate Code” - so that it can used for things like being
    displayed in your browser’s tab. Additionally, there are links to the source
    code for Mapbox’s JavaScript and CSS rules. If you copy either one of those
    links and paste it in a new tab in your browser, you’ll see a lot of raw
    code. By linking to the source, we avoid having to carry this text into our
    own document, while also being assured that the code we’re using is
    up-to-date.
  </head>

  <body>
    The body contains what you see formatted in your browser. In the code above,
    the body contains directions for rendering and displaying an interactive
    map centered on Vancouver.

    <div>
      This element states how tall and how wide the map should be on the screen.
    </div>

    <script>
      //Included in the body is a block of JavaScript that loads the map on the screen.
      //Continue to the next section for a better understanding of this script...
    </script>
  </body>
</html>
```
