<!------------------------------------------------------------>
<!--      FOSS4G 2014 - Quadcopter GIS on the cheap         -->
<!--      Target talk time - 20 min + 5 min questions       -->
<!------------------------------------------------------------>


<!------------------------------------------------------------>
<!-- Topic: Title slide -->

<img style="max-height: 300px;" src="images/quadcopter_cover.png">
<h2>Quadcopter GIS for less than $700</h2>
<h4>Hardware/Software to help map your local community</h4>
<p>
    <small>Aaron Racicot - <a href="mailto:aaronr@z-pulley.com">aaronr@z-pulley.com</a>
<br>
<a href="http://reprojected.com">reprojected.com</a> / <a href="http://twitter.com/reprojected">@reprojected</a> 
<br>
<a href="https://github.com/aaronr">github.com/aaronr</a>
<br><br>
<a href="http://aaronr.github.io/foss4g-2014/smalltown">aaronr.github.io/foss4g-2014/quadcopter</a>
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
<!-- Topic: Hardware setup ... -->

<img style="max-height: 450px;" src="images/phantom_fc40.jpg">
<br>
Phantom FC40

--SUBSLIDE--

<img style="max-height: 450px;" src="images/fc40_camera.jpg">
<br>
FPV camera (FC40)(720p)

--SUBSLIDE--

<img style="max-height: 450px;" src="images/canon.jpg">
<br>
Canon (16MP) downward facing camera (CHDK)

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chdk.png">
<br>
CHDK

--SUBSLIDE--

<img style="max-height: 450px;" src="images/z-pulley_phantom.jpg">
<br>
"The Rig"

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Why is this so interesting now ... -->

Why is this so interesting now...
<p class="fragment"><span style="color:#ff0000;">CHEAP!!</span></p>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/price_drop.jpg">
<br>
Aaron's Law of Quadcopter Pricing!

--SUBSLIDE--

<img style="max-height: 450px;" src="images/maps_fun.jpg">
<br>
Technology (Hardware and Software) are easy to use

--SUBSLIDE--

<h1><span style="color:#ff0000;">FUN!!!!!!!!!!</span></h1>

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Is it legal ... -->

<iframe width="100%" height="500px" frameBorder="0" src="https://www.mapbox.com/drone/no-fly/#10/45.4818/-122.6658"></iframe>
Where is it OK to fly
<br>
https://www.mapbox.com/drone/no-fly/

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Interesting workflows ... -->

<h2><span style="color:#ff0000;">Workflow</span></h2>
Panoramic image stitching

--SUBSLIDE--

<img style="max-height: 450px;" src="images/google.png">
<br>
... as good as Google gets

--SUBSLIDE--

<img style="max-height: 450px;" src="images/ice.png">
<br>
ICE

--SUBSLIDE--

<img style="max-height: 450px;" src="images/2ndstreet_stitch_small.jpg">

--SUBSLIDE--

<img style="max-height: 450px;" src="images/agisoft_stitch.png">
<br>
AgiSoft

--SUBSLIDE--

<img style="max-height: 450px;" src="images/photoscan_stitch_180_small.jpg">

--SUBSLIDE--

<img style="max-height: 450px;" src="images/langley_test_app_stitch.png">
<br>
Tile into an App!
<br>
qgis + nearblack + gdal2tiles + git pages

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Interesting workflows ... -->

<h2><span style="color:#ff0000;">Workflow</span></h2>
OSM data creation

--SUBSLIDE--

<img style="max-height: 450px;" src="images/qgis.png">
<br>
QGIS Warper

--SUBSLIDE--

<img style="max-height: 450px;" src="images/mapknitter1.png">
<br>
MapKnitter
http://mapknitter.org/

--SUBSLIDE--

<img style="max-height: 450px;" src="images/mapknitter2.png">
<br>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/id.png">
<br>
Edit in OSM
http://ideditor.com/

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Interesting workflows ... -->

<h2><span style="color:#ff0000;">Workflow</span></h2>
3D from Structure from Motion (SFM)

--SUBSLIDE--

<img style="max-height: 450px;" src="images/matches2.png">
<br>
Matching

--SUBSLIDE--

<img style="max-height: 450px;" src="images/vsfm_sparse.png">
<br>
Visual SFM
<br>
Sparse Point Cloud

--SUBSLIDE--

<img style="max-height: 450px;" src="images/vsfm_dense.png">
<br>
Dense Point Cloud

--SUBSLIDE--

<img style="max-height: 450px;" src="images/meshlab_ply.png">
<br>
MeshLab

--SUBSLIDE--

<img style="max-height: 450px;" src="images/meshlab_texture.png">

--SUBSLIDE--

<img style="max-height: 450px;" src="images/photoscan_image_sparse.png">
<br>
AgiSoft
<br>
Sparse Point Cloud

--SUBSLIDE--

<img style="max-height: 450px;" src="images/photoscan_image_dense.png">
<br>
Dense Point Cloud

--SUBSLIDE--

<img style="max-height: 450px;" src="images/photoscan_image_texture.png">
<br>
Textured Mesh


<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Future ... -->

<h2><span style="color:#ff0000;">More Examples</span></h2>

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chewy_textured.png">
<br>
Chewy

--SUBSLIDE--

<img style="max-height: 450px;" src="images/school.png">
<br>
School

--SUBSLIDE--

<img style="max-height: 450px;" src="images/farm.png">
<br>
Farm

--SUBSLIDE--

<img style="max-height: 450px;" src="images/ps_vsfm_compare.png">
<br>
Compare (VSFM vs PhotoScan)


<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Future ... -->

<h2><span style="color:#ff0000;">The Future</span></h2>
DEM's, geospatial models, 3D printing, etc

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chris_building.jpg">
<br>
3D Print Example (Chris Schmidt)

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chris_building_point.jpg">
<br>
Point Cloud

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chris_building_mesh.jpg">
<br>
Mesh

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chris_building_preprint.jpg">
<br>
Print Prep

--SUBSLIDE--

<img style="max-height: 450px;" src="images/chris_building_print.jpg">
<br>
Print!

<!------------------------------------------------------------>
--SLIDE--
<!-- Topic: Thank You -->

<img style="max-height: 150px;" src="images/z-pulley.png"><h1>Thank You !!!</h1><img style="max-height: 150px;" src="images/cugos.png">

