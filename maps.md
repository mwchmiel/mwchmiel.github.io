---
layout: default
---




<html>
  <head>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.3.1/leaflet.css" />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.3.1/leaflet.js"></script>
 <style>
#map {
    width: 1000px;
    height:800px;
}
</style>
  </head>
  <body>
    <div id="map"></div>
    <script>
      var map = L.map('map').setView([0, 0], 2);
	L.tileLayer('https://api.maptiler.com/maps/hybrid/{z}/{x}/{y}.jpg?key=XOnkBskT7Cy4ilY2wGew',{
	attribution: '<a href="https://www.maptiler.com/copyright/" target="_blank">&copy; MapTiler</a> <a href="https://www.openstreetmap.org/copyright" target="_blank">&copy; OpenStreetMap contributors</a>',
}).addTo(map)

	var wiripop = "<h3>Wind River Experimental Forest</h3><br/>  <img src='/images/STJA.png'/>";
	var saipanpop = "<h3>Saipan</h3></br> <img src='/images/COLK.png'/ width='300'>";

	var popOptions =
        {
        'minWidth': '300',
		'minHeight':'300',
        }

	var marker = L.marker([45.810511, -121.942358]).addTo(map).bindPopup(wiripop,popOptions);
	var marker = L.marker([15.185998, 145.771207]).addTo(map).bindPopup(saipanpop,popOptions);


    </script>
  </body>
</html>