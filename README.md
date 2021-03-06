# leaflet-distance-markers

Plugin for Leaflet to display markers along a route at equivalent distances.

forked from http://adoroszlai.github.com/leaflet-distance-markers/

## My Demo

https://jackdougherty.github.io/leaflet-distance-markers

```javascript
// use defaults
var line = L.polyline(coords);

// override defaults
var line = L.polyline(coords, {
	distanceMarkers: { showAll: 11, offset: 1600, cssClass: 'some-other-class' }
});

// show/hide markers on mouseover
var line = L.polyline(coords, {
	distanceMarkers: { lazy: true }
});
line.on('mouseover', line.addDistanceMarkers);
line.on('mouseout', line.removeDistanceMarkers);
map.fitBounds(line.getBounds());
map.addLayer(line);
```

## Options

 * **offset**: distance in meters between the markers (default: 1000 (= 1 km))
 * **showAll**: the zoom level at which all distance markers will be shown -- zooming out once from this level will remove approximately half of the markers (default: 12)
 * **lazy**: postpone adding the markers until Polyline.addDistanceMarkers is explicitly called (default: false)
 * **cssClass**: CSS class to set on marker icons

## Requirements

 * https://github.com/makinacorpus/Leaflet.GeometryUtil
