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
    
    /* Updated Map Container Styles */
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
    
    @media (max-width: 768px) {
        .container {
            flex-direction: column;
        }
        .map-container {
            height: 500px;
        }
    }
</style>

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
<script>
    // Initialize the map
    var map = L.map('marco-polo-map', {
        zoomControl: true,
        maxZoom: 18,
        minZoom: 2
    }).fitBounds([[21.9430, 105.8], [51.0, 142.0]]);

    // Add base layer
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map);

    // Custom style for Marco Polo locations
    var marcoPoloStyle = {
        radius: 6,
        fillColor: "#b7484b",
        color: "#333",
        weight: 1,
        opacity: 1,
        fillOpacity: 0.8
    };

    // Sample data (replace with your actual GeoJSON)
    var marcoPoloLocations = {
        "type": "FeatureCollection",
        "features": [
            {
                "type": "Feature",
                "properties": {
                    "Name": "Beijing (Canbaluc)",
                    "Description": "Marco Polo served here under Kublai Khan",
                    "Latitude (Y)": 39.9042,
                    "Longitude (X)": 116.4074
                },
                "geometry": {
                    "type": "Point",
                    "coordinates": [116.4074, 39.9042]
                }
            },
            {
                "type": "Feature",
                "properties": {
                    "Name": "Quanzhou (Çaiton)",
                    "Description": "Major port city described by Polo",
                    "Latitude (Y)": 24.9139,
                    "Longitude (X)": 118.5858
                },
                "geometry": {
                    "type": "Point",
                    "coordinates": [118.5858, 24.9139]
                }
            }
            // Add all your locations here
        ]
    };

    // Add locations to map
    L.geoJSON(marcoPoloLocations, {
        pointToLayer: function (feature, latlng) {
            return L.circleMarker(latlng, marcoPoloStyle);
        },
        onEachFeature: function (feature, layer) {
            var popupContent = `<h3>${feature.properties.Name}</h3>
                              <p>${feature.properties.Description || ''}</p>
                              <small>Lat: ${feature.properties['Latitude (Y)']}, Lon: ${feature.properties['Longitude (X)']}</small>`;
            layer.bindPopup(popupContent);
        }
    }).addTo(map);

    // Add legend
    var legend = L.control({position: 'bottomright'});
    legend.onAdd = function (map) {
        var div = L.DomUtil.create('div', 'info legend');
        div.innerHTML = '<h4>Marco Polo Locations</h4>';
        div.innerHTML += '<i style="background: #b7484b"></i> Documented locations';
        return div;
    };
    legend.addTo(map);
</script>
