## Sample Leaflet Map

<!DOCTYPE html>

<html>
<head>
    <title>Map of Points</title>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
</head>
<body>
    <div id="map" style="width: 100%; height: 600px;"></div>
    <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
    <script>
        var map = L.map('map').setView([51.505, -0.09], 13);

        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);

        var points = [
            [51.5, -0.09],
            [51.51, -0.1],
            [51.49, -0.08]
        ];

        points.forEach(function(point) {
            L.marker(point).addTo(map);
        });
    </script>
</body>
</html>
