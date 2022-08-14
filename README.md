# Leaflet.SimpleCRSMeasurement
A Leaflet.js plugin to perform measurements when using a simple CRS (coordinate system).

This is a fork of https://github.com/gokertanrisever/leaflet-ruler that I edited to work easily
when using non-standard maps with `L.CRS.Simple`.

## How to use

Add the dependencies to your map:

```
https://cdn.jsdelivr.net/gh/user/repo@version/file
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
    scale: 1.0,                   // scale distances to kilometer (or what you use in the formatter function)
    // custom function to return the distance as a string
    formatter: function(distance) {
        return distance.toFixed(1);            
    },
}
L.control.ruler(options).addTo(map);
```
