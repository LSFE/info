### Standardized storage of satellite data

<p align="justify">
One of the main issues in sharing data and tools between researchers has to do with the way we store and use data. Often, each researcher has its own data structure which makes it hard to apply a tool from another. As a consequence, adapting the work of someone else might be a bigger effort than writting a new function leading to an unnecessary replication of work. To avoid this, we developed <i>storeSat()</i> which creates a standized structure for satellite data and its corresponding metadata.
</p>

<br>

#### Data structure
<p align="justify">
The data for every satellite sensor stored through <i>LSFE</i> will have a comparable structure (Figure 1). As describe in the disgram below, the storage functions will create a folder for the sensor within which two folders will be created:
  
* SR - Folder where the surface reflectance data will be stored.
* infos - Folder where per-tile metadata for the downloaded acquisitions will be stored.

Then, inside <i>SR</i>, the function will create a folder for each tile and store the corresponding acquisitions within it. This function can be used in combination with <a href="https://github.com/LSFE/info/blob/master/example_3.md">lsfeData()</a> which eases the use of other useful tools (see <a href="">metaQuery()</a> and <a href="">stackSat()</a>).
</p>

<br>

<p align="center">
<img width="709" height="371" src="https://github.com/LSFE/info/blob/master/example-3_figure-1.jpg"></a>
</p>

<p align="center">
<sub>Figure 1 - Example data storage diagram for Landsat.</sub>
</p>

<br>

<p align="justify">
At the moment, <i>storeSat()</i> allows for the storage of Landsat MODIS 8-day (<a href="https://lpdaac.usgs.gov/dataset_discovery/modis/modis_products_table/mod09a1_v006">09A1</a>) and 16-day ((<a href="https://lpdaac.usgs.gov/dataset_discovery/modis/modis_products_table/mod13q1_v006">13Q1</a>) NDVI composites. The function requires the user to specify an input path (where the downloaded data is stored) and the output path (where the data will be sorted). Then, the user needs to specify the target sensor. Additionally, the user can choose to remove the original files after competion setting the keyword <i>remove.files</i> to TRUE. Besides the overall data structuring, <i>storeSat()</i> also translates existing quality information when necessary providing a binary layer within each acquisition folder (Figure 2). 
</p>
 
<br>
 
```R
# storage of landsat data
storeSat("path where tar.gz files are stored", "your output path", sensor="landsat", remove.files=TRUE)

# storage of modis data
storeSat("path where hdf files are stored", "your output path", sensor="landsat", remove.files=TRUE)
```

<br>

<p align="justify">

<br>

Click <a href="https://github.com/LSFE/LSFE-R">here</a> to return to <i>LSFE</i> main page.
