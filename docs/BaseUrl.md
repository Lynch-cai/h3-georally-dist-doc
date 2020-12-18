<h3>Base URL</h3>

When using GeoRally API, you’ll have to use URLs.
All GeoRally URLs have this form : ***https://georallyapi.herokuapp.com/***

> :point_right: **Example :** ***https://georallyapi.herokuapp.com/Monte-Carlo_SS1*** will generate the map for the race name “SS1 Monte-Carlo”

``` 
map.addSource('Session_1', {
        'type': 'geojson',
        'data': 'https://georallyapi.herokuapp.com/Monte-Carlo_SS1'
         });

                                                            