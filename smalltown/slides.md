<!------------------------------------------------------------>
<!--      FOSS4G 2014 - Small Town GIS leveraging GitHub    -->
<!--      Target talk time - 20 min + 5 min questions       -->
<!------------------------------------------------------------>


<!------------------------------------------------------------>
<!-- Topic: Title slide -->

<img style="max-height: 400px;" src="images/cover.png">
<h2>Small Town GIS leveraging GitHub</h2>
<p>
    <small>Aaron Racicot - <a href="mailto:aaronr@z-pulley.com">aaronr@z-pulley.com</a>
<br>
<a href="http://reprojected.com">reprojected.com</a> / <a href="http://twitter.com/reprojected">@reprojected</a> 
<br>
<a href="https://github.com/aaronr">github.com/aaronr</a>
<br><br>
<a href="http://aaronr.github.io/foss4g-2014/smalltown">aaronr.github.io/foss4g-2014/smalltown</a>
</small>
</p>

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Introduce myself -->

<h1>Who I am?</h1>

<ul>
  <li><strong>SW <span style="color:#ff0000;">Developer</span></strong></li>
  <li><strong>Environmental <span style="color:#ff0000;">Scientist</span></strong></li>
  <li><strong>Open Source <span style="color:#ff0000;">Advocate</span></strong></li>
</ul>

--SUBSLIDE--

  <h3>Computer Science</h3>
  <h2><span style="color:#ff0000;">Bridging the Gap</span></h2>
  <h3>Environmental Science</h3>

--SUBSLIDE--
<img src="images/whoami.png">


<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Target Audience -->

<img style="max-height: 450px;" src="images/langley_overview.png">
<br>
Our "Small Town" - 1000 residents

--SUBSLIDE--

<img style="max-height: 450px;" src="images/langley_location.png">
<br>
Washington State - North of Seattle

--SUBSLIDE--

<img style="max-height: 450px;" src="images/langley_city_limits.png">
<br>
1 Square Mile

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: How we started -->

<h2><span style="color:#ff0000;">How this started</span></h2>
Student Internship

--SUBSLIDE--

<h2><span style="color:#ff0000;">Where we want to go</span></h2>
Partnerships with local Government

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Needs -->

<h2>What our small town does not have...</h2>
<p class="fragment">Money</p>
<p class="fragment">Resources (People)</p>
<p class="fragment">Resources (Technology)</p>

--SUBSLIDE--

<h2>What our small town needs...</h2>
<p class="fragment">Inexpensive solutions</p>
<p class="fragment">Data normalization</p>
<p class="fragment">Data access</p>
<p class="fragment">Simple Applications</p>

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: GitHub ... -->

<img style="max-height: 200px;" src="images/github-logo.png">
<br>
<p class="fragment">Version Control (Data and Applications)</p>
<p class="fragment">Hosting (GitHub Pages)</p>
<p class="fragment">Open at heart!</p>
<p class="fragment">Free!!!</p>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_plans.png">
<br>
Work in the open... for FREE!

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_pages.png">
<br>
Leveraging GitHub Pages for hosting!

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Geo at GitHub -->

<img style="max-height: 450px;" src="images/github_geo.png">
<br>
Geo at Github

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_geo_preview.png">
<br>
Preview data

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_diff.gif">
<br>
Diff GeoJSON

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Bring the two together -->

<h2><span style="color:#ff0000;">Workflow</span></h2>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_data.png">
<br>
Add Data

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_geo_preview.png">
<br>
Preview

--SUBSLIDE--

<img style="max-height: 450px;" src="images/geojson.io.png">
<br>
Edit Data (geojson.io)

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_diff.gif">
<br>
Diff Data

--SUBSLIDE--

<img style="max-height: 450px;" src="images/github_app.png">
<br>
Build Apps!


<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: -->

<h2><span style="color:#ff0000;">Data</span></h2>
GeoJSON + Tile Sets

--SUBSLIDE--

<h2><span style="color:#ff0000;">GeoJSON</span></h2>

Convert and reproject to WGS84 lat/lon (EPSG:4326)

<pre><code>
for f in *.shp; do ogr2ogr -f "GeoJSON" -s_srs EPSG:2285 ...
-t_srs EPSG:4326 ${f/.shp}_4326.geojson $f; done
</code></pre>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/new_repo.png">
<br>
Create repo on GitHub

--SUBSLIDE--

<pre><code>
git clone git@github.com:langleywa/gisdata.git
cd gisdata
mv ~/mylayer.geojson .
git add mylayer.geojson
git commit -m "Yes... DATA"
git push
</code></pre>

--SUBSLIDE--

<pre><code>
git checkout -b gh-pages
git push origin gh-pages
</code></pre>

--SUBSLIDE--

http://langleywa.github.io/gisdata/geojson/citylimitsline_4326.geojson
<br>
<img style="max-height: 450px;" src="images/geojson.png">

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: -->

<h2><span style="color:#ff0000;">Tile Sets</span></h2>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/qgis.png">
<br>
Geo reference your data

--SUBSLIDE--

<pre><code>
nearblack -of GTiff -setalpha -o outfile infile
</code></pre>

--SUBSLIDE--

<pre><code>
gdal2tiles.py --profile=mercator -z 1-22 yourmap.tif outputfolder
</code></pre>

--SUBSLIDE--

<pre><code>
git add outputfolder
git commit -m "Yes... TILE DATA"
git push
</code></pre>

--SUBSLIDE--

<pre><code>
git checkout gh-pages
git merge master
git push origin gh-pages
</code></pre>

--SUBSLIDE--

http://langleywa.github.io/gisdata/tiles/langley-2nd-street-2014/21/335500/1368498.png
<br>
<img style="max-height: 450px;" src="images/tile.png">

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Examples adding data-->

GeoJson
<pre><code>
var featureLayer = L.mapbox.featureLayer()
    .loadURL('/gisdata/geojson/citylimitsline_4326.geojson')
    .addTo(map);
</code></pre>

--SUBSLIDE--

Tiles
<pre><code>
var tileLayer = L.tileLayer('/gisdata/tiles/langley-2nd-street-2014/{z}/{x}/{y}.png', 
    {tms: true, minZoom:1, maxZoom:22, bounds:bounds}).addTo(map);
</code></pre>

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Examples -->

Test App<br>
<small>http://langleywa.github.io/apps/test/</small>

Example Data URLs<br>
<small>http://langleywa.github.io/gisdata/geojson/historicinventory_4326.geojson</small>
<small>http://langleywa.github.io/gisdata/tiles/langley-2nd-street-2014/16/10484/42765.png</small>

geojson.io<br>
<small>http://geojson.io/#id=github:langleywa/gisdata/blob/gh-pages/geojson/historicinventory_4326.geojson&map=19/48.04109/-122.40962</small>

Diff URL<br>
<small>https://github.com/langleywa/gisdata/commit/9e74d8c5e4d9f906c20e1d4778077e8578d58d1c?short_path=e5eee6f#diff-e5eee6f691fac526315233e6a5fcf251</small>


<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Thank You -->

<img style="max-height: 150px;" src="images/z-pulley.png"><h1>Thank You !!!</h1><img style="max-height: 150px;" src="images/cugos.png">
