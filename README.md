Leaflet.Control.Search
============

#What
A leaflet control that search markers/features location by cutstom property.
With ajax/jsonp autocompletion and json fields re-mapping

Tested in Leaflet 0.5.1


#Where

**Demos:**  
[labs.easyblog.it/maps/leaflet-search](http://labs.easyblog.it/maps/leaflet-search/)

**Source code:**  
[Github](https://github.com/stefanocudini/leaflet-search)  
[Bitbucket](https://bitbucket.org/zakis_/leaflet-search)  
[NPM](https://npmjs.org/package/leaflet-search)  

#How
Insert leaflet-search.css styles to your css page

Adding the search control to the map:

```
map.addControl( new L.Control.Search({layer: searchLayer}) );
//searchLayer if a L.LayerGroup contains searched markers
```

other examples:
```
map.addControl( new L.Control.Search({url: 'search.php?q={s}'}) );
//ajax request to search.php for retrieve elements locations

map.addControl( new L.Control.Search({
		url: 'http://nominatim.openstreetmap.org/search?format=json&q={s}',
		jsonpParam: 'json_callback',
		propertyName: 'display_name',
		propertyLoc: ['lat','lon']
	}) );
//jsonp request to 3rd party service, implements Geocode Searching using OSM API
```

