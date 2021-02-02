---
layout: default
---

<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.3.1/leaflet.css" />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.3.1/leaflet.js"></script>
    <style>
      #map {position: absolute; top: 0; right: 0; bottom: 0; left: 0;}
    </style>
  </head>
  <body>
    <div id="map"></div>
    <script>
      var map = L.map('map').setView([-16.768995, -110.905272], 3);
	L.tileLayer('https://api.maptiler.com/maps/hybrid/{z}/{x}/{y}.jpg?key=XOnkBskT7Cy4ilY2wGew',{
	attribution: '<a href="https://www.maptiler.com/copyright/" target="_blank">&copy; MapTiler</a> <a href="https://www.openstreetmap.org/copyright" target="_blank">&copy; OpenStreetMap contributors</a>',
}).addTo(map)

	var stjapop = "Wind River Experimental Forest<br/><img src='/maps/images/STJA.png' width='200px'/>";
	var colkpop = "The Island of Saipan<br/><img src='/maps/images/COLK.png' height='200px'/>";

	var marker = L.marker([45.810511, -121.942358]).addTo(map).bindPopup(stjapop);
	var marker = L.marker([15.185998, 145.771207]).addTo(map).bindPopup(colkpop);


    </script>
  </body>
</html>

