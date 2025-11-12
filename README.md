<!DOCTYPE html>
<html>
<head>
  <title>Mapa Interactivo</title>
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
  <style>
    #map { height: 500px; width: 100%; }
  </style>
</head>
<body>
  <h2>Mi mapa interactivo</h2>
  <div id="map"></div>

  <script>
    // Crear mapa centrado
    var map = L.map('map').setView([8.9833, -79.5167], 8); // Panamá

    // Cargar capa base
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: 'Mapa © OpenStreetMap'
    }).addTo(map);

    // Agregar marcador
    L.marker([8.9833, -79.5167]).addTo(map)
      .bindPopup('<b>Ciudad de Panamá</b><br>Capital de Panamá.')
      .openPopup();
  </script>
</body>
</html>
