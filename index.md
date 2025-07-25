<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapping Marco Polo's Divisament dou Monde</title>
    <style>
        /* GitHub Pages container override */
        .Layout-main {
            margin-top: 0 !important;
            padding-top: 0 !important;
        }
        
        /* Your existing styles */
        body {
            font-family: 'Georgia', serif;
            line-height: 1.6;
            color: #333;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f7;
        }
        .header-image {
            width: 100%;
            max-height: 400px;
            object-fit: cover;
            margin-bottom: 30px;
            border-radius: 4px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        .container {
            display: flex;
            gap: 40px;
        }
        .column {
            flex: 1;
            display: flex;
            flex-direction: column;
        }
        .paragraph-pair {
            display: flex;
            flex-direction: column;
            margin-bottom: 20px;
        }
        h1 {
            font-family: 'Palatino Linotype', 'Book Antiqua', serif;
            text-align: center;
            margin: 20px 0 5px 0;
            color: #444;
            font-style: normal;
        }
        h2.subtitle {
            font-family: 'Palatino Linotype', 'Book Antiqua', serif;
            text-align: center;
            margin: 0;
            color: #666;
            font-size: 1.2em;
            font-weight: normal;
        }
        h2.developer {
            font-family: 'Palatino Linotype', 'Book Antiqua', serif;
            text-align: center;
            margin: 0 0 20px 0;
            color: #666;
            font-size: 1em;
            font-weight: normal;
            font-style: italic;
        }
        h1 em {
            font-style: italic;
        }
        p {
            text-align: justify;
            margin: 0 0 10px 0;
        }
        
        /* Map Container Styles */
        .map-container {
            width: 100%;
            height: 700px;
            margin: 40px 0;
            border-radius: 4px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            overflow: hidden;
            position: relative;
        }
        #marco-polo-map {
            width: 100%;
            height: 100%;
            background: #f8f4e8;
        }
        
        /* QGIS2Web styles */
        .leaflet-container {
            font: 12px/1.5 "Helvetica Neue", Arial, Helvetica, sans-serif;
        }
        .leaflet-popup-content {
            width: auto !important;
            margin: 13px 19px;
        }
        .leaflet-popup-content-wrapper {
            border-radius: 2px;
        }
        .css_MarcoPoloLocalitiesCSVFoglio1_1 {
            color: #323232;
            font-size: 10pt;
            font-weight: bold;
            font-family: 'Open Sans', sans-serif;
            background: transparent;
            border: none;
            box-shadow: none;
            text-shadow: 1px 1px 0px rgba(255,255,255,0.7);
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            .map-container {
                height: 500px;
            }
        }
    </style>
</head>
<body>
    <h1><em>Mapping Marco Polo's Divisament dou Monde</em></h1>
    <h2 class="subtitle">A GitHub repository for the <a href="https://www.mappingpolo.com" target="_blank" style="color: #3366cc; text-decoration: none;">Mapping Polo project</a></h2>
    <h2 class="developer">Developer and PI: Tommaso Pepe, <a href="https://uibe.academia.edu/TommasoPepe" target="_blank" style="color: #3366cc; text-decoration: none;">https://uibe.academia.edu/TommasoPepe</a></h2>

    <div class="container">
        <div class="column">
            <div class="paragraph-pair">
                <p>Written within the walls of a Genoese prison the end of the 13th century, Marco Polo's Divisament dou Monde ("The Description of the World") represents one of the most emblematic texts in the travel and geographical literature of the European Middle Ages.</p>
            </div>
            
            <div class="paragraph-pair">
                <p>Blending factual observation and an intricate network of cultural imaginaries, the Divisament dou Monde offers a description of Asia as it was perceived through the eyes of a European traveler at the end of the 13th century. Polo's text accumulates a staggering mass of cultural, historic, economic, and religious information relative to more than two hundred localities: cities, rivers, kingdoms, islands, regions that range from Indonesia to Central Asia. Names such as "Japan", "Java", "Sumatra", "Tibet", "Bengala" entered the Western cultural tradition through this text, along with the first biography of Siddhartha Gautama recorded in a European source.</p>
            </div>
        </div>
        
        <div class="column">
            <div class="paragraph-pair">
                <p>马可波罗的《Divisament dou Monde》写于 13 世纪末热那亚监狱的围墙内，是欧洲中世纪旅行和地理文学中最具代表性的作品之一。</p>
            </div>
            
            <div class="paragraph-pair">
                <p>《Divisament dou Monde》融事实观察和错综复杂的文化想象于一体，描述了 13 世纪末一位欧洲旅行者眼中的亚洲。马可波罗的文字蕴含了丰富的文化、历史、经济和宗教内容，而这些内容涉及到两百多个地方：包括从印度尼西亚到中亚地区的城市、河流、王国、岛屿。"日本"、"爪哇岛"、"苏门答腊岛"、"西藏"、"孟加拉 "等地名通过该书进入西方文化传统中，同时书中也记载了释迦牟尼的首部传记。</p>
            </div>
        </div>
    </div>

    <!-- Marco Polo Map Container -->
    <div class="map-container">
        <div id="marco-polo-map"></div>
    </div>

    <div class="container">
        <div class="column">
            <div class="paragraph-pair">
                <p>This digital humanities project aims to present a first georeferenced map of the localities described by Polo in his book, visualizing the literary geographies of the Divisament dou Monde.</p>
            </div>
            
            <div class="paragraph-pair">
                <p>The project is being developed on an ArcGIS platform and is ongoing.</p>
            </div>
        </div>
        
        <div class="column">
            <div class="paragraph-pair">
                <p>该数字化人文项目旨在为马可波罗在其著作中描述的地点提供第一张地理参考地图，将《Divisament dou Monde》这部地理文学作品可视化。</p>
            </div>
            
            <div class="paragraph-pair">
                <p>该项目目前正在 ArcGIS 平台上进行。</p>
            </div>
        </div>
    </div>

    <!-- Map Scripts -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/autolinker@3.14.2/dist/Autolinker.min.js"></script>
    
    <!-- Your QGIS2Web data and scripts -->
    <script>
    // Marco Polo Localities Data
    var json_MarcoPoloLocalitiesCSVFoglio1_1 = {
        "type": "FeatureCollection",
        "features": [
            // Your complete feature data goes here
            // Example feature:
            {
                "type": "Feature",
                "properties": {
                    "Name": "Beijing (Canbaluc)",
                    "Latitude (Y)": 39.9042,
                    "Longitude (X)": 116.4074
                },
                "geometry": {
                    "type": "Point",
                    "coordinates": [116.4074, 39.9042]
                }
            },
            // Add all your features from MarcoPoloLocalitiesCSVFoglio1_1.js
        ]
    };
    </script>
    
    <script>
    // Initialize the map with your original QGIS settings
    var map = L.map('marco-polo-map', {
        zoomControl: false,
        maxZoom: 28,
        minZoom: 1
    }).fitBounds([[-21.01662037982929, -10.272148768597788], [34.887839911223146, 80.47482199547952]]);
    
    // Add base layer
    var layer_OpenStreetMap_0 = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        opacity: 1.0,
        attribution: '',
        minZoom: 1,
        maxZoom: 28,
        minNativeZoom: 0,
        maxNativeZoom: 19
    }).addTo(map);
    
    // Add zoom control
    L.control.zoom({ position: 'topleft' }).addTo(map);
    
    // Function to handle popups (from your original QGIS export)
    function pop_MarcoPoloLocalitiesCSVFoglio1_1(feature, layer) {
        var popupContent = '<table>\
                <tr>\
                    <th scope="row">Name</th>\
                    <td>' + (feature.properties['Name'] !== null ? Autolinker.link(String(feature.properties['Name']).replace(/'/g, '\'').toLocaleString() : '') + '</td>\
                </tr>\
                <tr>\
                    <td colspan="2">Latitude: ' + (feature.properties['Latitude (Y)'] !== null ? Autolinker.link(String(feature.properties['Latitude (Y)']).replace(/'/g, '\'').toLocaleString() : '') + '</td>\
                </tr>\
                <tr>\
                    <td colspan="2">Longitude: ' + (feature.properties['Longitude (X)'] !== null ? Autolinker.link(String(feature.properties['Longitude (X)']).replace(/'/g, '\'').toLocaleString() : '') + '</td>\
                </tr>\
            </table>';
        
        layer.bindPopup(popupContent, { maxHeight: 400 });
    }
    
    // Style for Marco Polo locations
    function style_MarcoPoloLocalitiesCSVFoglio1_1_0() {
        return {
            radius: 4.0,
            opacity: 1,
            color: 'rgba(35,35,35,1.0)',
            dashArray: '',
            lineCap: 'butt',
            lineJoin: 'miter',
            weight: 1,
            fill: true,
            fillOpacity: 1,
            fillColor: 'rgba(183,72,75,1.0)',
            interactive: true,
        }
    }
    
    // Add Marco Polo locations layer
    var layer_MarcoPoloLocalitiesCSVFoglio1_1 = L.geoJson(json_MarcoPoloLocalitiesCSVFoglio1_1, {
        onEachFeature: pop_MarcoPoloLocalitiesCSVFoglio1_1,
        pointToLayer: function (feature, latlng) {
            return L.circleMarker(latlng, style_MarcoPoloLocalitiesCSVFoglio1_1_0());
        }
    }).addTo(map);
    
    // Add labels if needed (simplified from your original)
    layer_MarcoPoloLocalitiesCSVFoglio1_1.eachLayer(function(layer) {
        if (layer.feature.properties['Name']) {
            layer.bindTooltip(layer.feature.properties['Name'], {
                permanent: true,
                direction: 'top',
                className: 'css_MarcoPoloLocalitiesCSVFoglio1_1'
            });
        }
    });
    </script>
</body>
</html>
