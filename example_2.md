### Which tiles do I need? Determining data requirements

<p align="justify">
One step that is often required at the beggining of any remote sensing research work is determining data requirements. <i>satQuery</i> supports this task by helping in determing which tiles are required to cover a given study site. Let's consider the example shapefile provided here and load it in R with the example code below.
</p>



Then, let's check which tiles we require for this study site. for MODIS, Landsat and Sentinel-2. <i>satQuery</i> deals with satellite data for which a shapefile with acquisition footprints is available. At the moment, the function provides access to tile information from these sensors through the keyword <i>sensor</i>, as examplified below. Note that the projection of the reference extent is irrelevant as this will be transformed in accordance with the projection of the tile shapefile.




While the function only provides access to these three sensors it is not restricted to them. Accounting for other sensors, the function allows the users to provide their own shapefile using the keyword <i>shp>/i> as shown in the example below.
