# Leaflet.SimpleCRSMeasurement
A Leaflet.js plugin to perform measurements when using a simple CRS (coordinate system).

This is a fork of https://github.com/gokertanrisever/leaflet-ruler that I edited to work easily with `L.CRS.Simple`, when using non-standard maps like drawn maps or game maps.

![screenshot](https://user-images.githubusercontent.com/33519926/184546111-94527649-f8cd-4996-b22d-03c550f77a07.PNG)

## How to use

Add the dependencies to your map:

```
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/conengmo/Leaflet.SimpleCRSMeasurement/leaflet-ruler.css">
<script src="https://cdn.jsdelivr.net/gh/conengmo/Leaflet.SimpleCRSMeasurement/leaflet-ruler.js"></script>
```

Load the control:

```
L.control.ruler().addTo(map);
```

## Options

```
let options: {
    position: 'topright',         // Leaflet control position option
    circleMarker: {               // Leaflet circle marker options for points used in this plugin
        color: 'red',
        radius: 2
    },
    lineStyle: {                  // Leaflet polyline options for lines used in this plugin
        color: 'red',
        dashArray: '1,6'
    },
    // to get a meaningful distance you will have to provide a conversion factor:
    scale: 1.0,                   
    // custom function to return the distance as a string
    formatter: function(distance) {
        return distance.toFixed(1);            
    },
}
L.control.ruler(options).addTo(map);
```
