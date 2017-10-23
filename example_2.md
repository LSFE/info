### Which tiles do I need? Determining data requirements

<p align="justify">
One step that is often required at the beggining of any remote sensing research work is determining data requirements. <i>satQuery</i> supports this task by helping in determing which tiles are required to cover a given study site. Let's consider the example shapefile provided <a href="https://github.com/LSFE/info/blob/master/example-1_data.zip">here</a> and load it in R with the example code below.
</p>

```R
# read shapefile
study.shp <- shapefile('study-site.shp')
```

<p align="justify">
Then, let's check which tiles we require for this study site. for MODIS, Landsat and Sentinel-2. <i>satQuery</i> deals with satellite data for which a shapefile with acquisition footprints is available. At the moment, the function provides access to tile information from these sensors through the keyword <i>sensor</i>, as examplified below. Note that the projection of the reference extent is irrelevant as this will be transformed in accordance with the projection of the tile shapefile.
</p>

```R
# check MODIS tiles
satQuery(ext=study.shp, sensor="modis")

# check Landsat tiles
satQuery(ext=study.shp, sensor="landsat")

# check Sentinel-2 tiles
satQuery(ext=study.shp, sensor="sentinel2")
```

<p align="justify">
While the function only provides access to these three sensors it is not restricted to them. Accounting for other sensors, the function allows the users to provide their own shapefile using the keyword <i>shp>/i> as shown in the example below. Here, you need to specicify the shapefile (<i>shp>/i>) and the name of the column where the tile names are stored (<i>tile<i>).
</p>
  

```R
# read Landsat shapefile from package
file <- system.file('extdata', 'landsat-tiles.shp', package="rsMove")
tile.shp <- shapefile(file)

# perform query
satQuery(ext=study.shp, shp=tile.shp, tile="tile")
```
 
The full example code can be downloaded <a href="">here</a>.
  
</b>

Click <a href="https://github.com/LSFE/LSFE-R">here</a> to return to <i>LSFE</i> main page.
