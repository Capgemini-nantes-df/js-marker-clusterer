**Please note:** This repository is not currently maintained, and is kept for historical purpose only.

Marker Clusterer – A Google Maps JavaScript API utility library
==============

A Google Maps JavaScript API v3 library to create and manage per-zoom-level clusters for large amounts of markers.
![Analytics](https://maps-ga-beacon.appspot.com/UA-12846745-20/js-marker-clusterer/readme?pixel)

[Reference documentation](https://googlemaps.github.io/js-marker-clusterer/docs/reference.html)

## Usage

index.html

    ...

    <div id="map-container"><div id="map"></div></div>
    <script src="markerclusterer.js"></script>
    <script>
        function initialize() {
            var center = new google.maps.LatLng(51.5074, 0.1278);

            var map = new google.maps.Map(document.getElementById('map'), {
              zoom: 3,
              center: center,
              mapTypeId: google.maps.MapTypeId.ROADMAP
            });

            var markers = [];
            var marker = new google.maps.Marker({
                position: new google.maps.LatLng(51.5074, 0.1278)
            });
            markers.push(marker);

            var options = {
                imagePath: 'images/m',
                centroidCenter:'true'
            };

            var markerCluster = new MarkerClusterer(map, markers, options);
        }

        google.maps.event.addDomListener(window, 'load', initialize);
    </script>
    ...
    
