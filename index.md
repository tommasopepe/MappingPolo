<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mapping Marco Polo's <i>Divisament dou Monde</i></title>
    <style>
        /* COMPLETE GITHUB HEADER SUPPRESSION */
        .Header, 
        .header, 
        .gh-header, 
        .repohead, 
        .repository-content > h1,
        .pagehead,
        .js-repo-nav {
            display: none !important;
            visibility: hidden !important;
            height: 0 !important;
            padding: 0 !important;
            margin: 0 !important;
            border: 0 !important;
        }
        
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
        
        /* New Map Container Styles */
        .map-container {
            width: 100%;
            height: 600px;
            margin: 40px 0;
            border-radius: 4px;
            box-shadow: 0 2px 15px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        iframe {
            border: none;
            width: 100%;
            height: 100%;
        }
        
        @media (max-width: 768px) {
            .container {
                flex-direction: column;
            }
            .map-container {
                height: 400px;
            }
        }
    </style>
</head>
<body>
    <img src="https://static.wixstatic.com/media/75d65a_4c4d7e4243a44932ba2fc1f90d4aac29~mv2.jpg/v1/fill/w_2560,h_1272,al_c,q_90,usm_0.66_1.00_0.01,enc_avif,quality_auto/75d65a_4c4d7e4243a44932ba2fc1f90d4aac29~mv2.jpg" 
         alt="Marco Polo's Journey" 
         class="header-image">
    
    <h1><em>Marco Polo's Divisament dou Monde</em></h1>
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
    
    <!-- New Map Section -->
    <div class="map-container">
        <iframe src="https://tommasopeojcts.maps.arcgis.com/apps/mapviewer/index.html?webmap=0f8e01072cb04c308971aebf99646cc7" 
                title="Marco Polo's Journey Map"
                allow="geolocation"
                allowfullscreen>
        </iframe>
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
</body>
</html>
