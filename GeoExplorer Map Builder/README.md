# GeoExplorer Map Builder

Build custom responsive web mapping applications without any coding!

A simple, lightweight tool for quickly standing up responsive web mapping applications _without having to write any code_. Built on the [Google Maps JavaScript API](https://developers.google.com/maps/web/), this utility lets you configure your settings via simple URL parameters. Feed it a source data file in GeoJSON format (or CSV with `latitude` & `longitude` columns), give it a title, icon, and tell it which data fields you want to show, and you get a responsive, mobile-friendly "mapzap" for viewing and interacting with your data. Your mapzap can be shared, embedded into websites and blogs, and added to your mobile device's homescreen for a native, full screen experience. Use [geojson.io](http://geojson.io/), [GeoEditor](https://geoeditor.maptiler.com), [Fulcrum](http://www.fulcrumapp.com/), [QGIS](https://www.qgis.org/) or any other modern mapping tool to generate your GeoJSON, place it on a web server, push it to GitHub, Google Drive, Dropbox, etc. or save it as a Gist and quickly wrap it up as a responsive web app.

### Get Starteds

Use the Builder Tool to quickly build your Map!

You can also download or fork this repo and host your own version. If you self-host, please use your own Google Maps API key.

### Features

- Fullscreen web app with responsive navbar, modal popups, and map/table/split views.
- Built on the incredibly popular [Bootstrap](http://getbootstrap.com/) and [Google Maps](https://developers.google.com/maps/web/) frameworks.
- Configure everything via URL parameters (no coding necessary)!
- Define data source, app title, icon, display fields/properties & data attribution manually or with the Map Builder Tool.
- Completely client-side, can be hosted for free on [GitHub Pages](https://pages.github.com/)
- Supports custom feature styling and [StreetView](https://www.google.com/streetview/understand/) integration
- Interactive feature table with filtering, sorting, and column toggling via [Bootstrap Table](http://bootstrap-table.wenzhixin.net.cn/)


### JSON Style Options

Feature styling per the [google.maps.Data.StyleOptions](https://developers.google.com/maps/documentation/javascript/3.exp/reference#Data.StyleOptions) object specification. You can also categorically style features by defining an object with `property` and `values` properties. Values should be an object of values and corresponding CSS3 colors or URLs to marker images.

#### Single Style Example (SVG symbols)

```js
{
  "fillColor": "blue",
  "fillOpacity": 0.2,
  "strokeColor": "blue",
  "strokeOpacity": 1,
  "strokeWeight": 2,
  "icon": {
    "path": 0,
    "scale": 7,
    "strokeColor": "white",
    "strokeWeight": 1,
    "fillColor": "blue",
    "fillOpacity": 1
  }
}
```

#### Single Style Example (Image marker)

```js
{
  "icon": "https://maps.gstatic.com/mapfiles/ms/micons/blue.png"
}
```

#### Categorized Style Example (SVG symbols)

```js
{
  "property": "degree_of_damage",
  "values": {
    "Destroyed": "#DA0796",
    "Major": "#CB0D0C",
    "Minor": "#FF8819",
    "Affected": "#FFD300",
    "Inaccessible": "#B3B3B3",
    "No Visible Damage": "#87D30F"
  }
}
```

#### Categorized Style (Image markers)

```js
{
  "property": "degree_of_damage",
  "values": {
    "Destroyed": "https://maps.gstatic.com/mapfiles/ms/micons/pink.png",
    "Major": "https://maps.gstatic.com/mapfiles/ms/micons/red.png",
    "Minor": "https://maps.gstatic.com/mapfiles/ms/micons/orange.png",
    "Affected": "https://maps.gstatic.com/mapfiles/ms/micons/yellow.png",
    "Inaccessible": "https://maps.gstatic.com/mapfiles/ms/micons/grey.png",
    "No Visible Damage": "https://maps.gstatic.com/mapfiles/ms/micons/green.png"
  }
}
```
