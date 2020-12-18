## How to use GeoRally

After Sign in / Log in, you’ll have to follow a simple step to install your **Geo**Rally service.

> **Step :one: : Add the GeoRally source with type geojson.**</br>
***'Session1' is your ID***
```
     map.addSource('Session_1', {
       'type': 'geojson',
       'data': 'https://georallyapi.herokuapp.com/Monte-Carlo_SS1'
       });
```
<br/><br/>
> **Step :two: : To add the icons, add the loads images.**

```
 map.loadImage(
                'https://i.postimg.cc/rsRdym57/point-attention-1.png',
                function (error, image) {
                    if (error) throw error;
                    map.addImage('red', image);

                    map.loadImage(
                        'https://i.postimg.cc/sDmMYP8m/orange.png',
                        function (error2, image2) {
                            if (error2) throw error2;

                            map.addImage('orange', image2);

                            map.loadImage(
                                'https://i.postimg.cc/NF75PR0g/green.png',
                                function (error3, image3) {
                                    if (error3) throw error3;

                                    map.addImage('green', image3);


                                    map.loadImage(
                                        'https://i.postimg.cc/T2rLwvJZ/eboulement.png',
                                        function (error4, image4) {
                                            if (error4) throw error4;

                                            map.addImage('eboulement', image4);

                                            map.loadImage(
                                                'https://i.postimg.cc/HsdJ8vSj/eboulement-orange.png',
                                                function (error5, image5) {
                                                    if (error5) throw error5;

                                                    map.addImage('eboulement-orange',
                                                        image5);

                                                    map.loadImage(
                                                        'https://i.postimg.cc/q75qNC0j/point-drapeau.png',
                                                        function (error6, image6) {
                                                            if (error6) throw error6;

                                                            map.addImage('start',
                                                                image6);
                                                      });

                                                })

                                        })

                                })

                        })


                })


```
<br/><br/>
> **Step :three: : Add Mapbox layer to get colors data and logo type.**
```
   map.addLayer({
                                                                'id': 'points',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'red',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#ffffff"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ], 'red'
                                                                ]
                                                            });

                                                            map.addLayer({
                                                                'id': 'points2',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'orange',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#ffffff"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ],
                                                                    'orange'
                                                                ]
                                                            });

                                                            map.addLayer({
                                                                'id': 'points3',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'green',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#ffffff"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ],
                                                                    'green'
                                                                ]
                                                            });

                                                            map.addLayer({
                                                                'id': 'points4',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'eboulement',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#ffffff"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ],
                                                                    'eboulement'
                                                                ]
                                                            });

                                                            map.addLayer({
                                                                'id': 'points5',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'start',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#277EFF"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ],
                                                                    'start'
                                                                ]
                                                            });

                                                            map.addLayer({
                                                                'id': 'points6',
                                                                'type': 'symbol',
                                                                'source': 'Session_1',
                                                                'layout': {
                                                                    'icon-image': 'eboulement-orange',
                                                                    // get the title name from the source's "title" property
                                                                    'text-field': [
                                                                        'get',
                                                                        'Name'
                                                                    ],
                                                                    'text-font': [
                                                                        'Open Sans Semibold',
                                                                        'Arial Unicode MS Bold'
                                                                    ],
                                                                    'text-offset': [
                                                                        0,
                                                                        1.25
                                                                    ],
                                                                    'text-anchor': 'top',

                                                                },
                                                                'paint': {
                                                                    "text-color": "#ffffff"
                                                                },

                                                                'filter': ['==',
                                                                    ['get',
                                                                        'icon-type'
                                                                    ],
                                                                    'eboulement-orange'
                                                                ]
                                                            });

```
<br/><br/>

**If you want to use GeoRally somewhere else**

> Step :four: : Use this code
```
var request = new XMLHttpRequest();
request.onreadystatechange = function() {
    if (this.readyState == XMLHttpRequest.DONE && this.status == 200) {
        var response = JSON.parse(this.responseText);
        console.log(response.current_condition.condition);
    }
};
request.open("GET", "https://georallyapi.herokuapp.com/{the_stage");
request.send();
```