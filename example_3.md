### Standardized storage of satellite data

<p align="justify">
One of the main issues in sharing data and tools between researchers has to do with the way we store and use data. Often, each researcher has its data structure which makes it hard to apply re-apply a tool. As a consequence, adapting the work of someone else might be a bigger effort than writting our own functions leading to an unnecessary replication of work.
To avoid this, we developed a series of tools to create a standized structure for satellite data and its corresponding metadata. Ideally, this function can be used in combination with <i>lsfeData()</i> (see <a href="https://github.com/LSFE/info/blob/master/example_3.md">here</a>). See below for examples on the sensors considered in <i>LSFE</i>.
</p>

#### Landsat
<p align="justify">
Using <i>storeLandsat()</i> the storage of Landsat data is made a lot easier. This function requires the user to specify an input path where the packed landsat data is stored and an output directory (e.g. <i>01_DATA</i> provided by <i>lsfeData()</i>). Using this simple information input, the function will generate a folder called <i>"Landsat"</i> within which two folder will be created:
  
* sr - Folder where the surface reflectance data will be stored.
* infos - Folder where per-tile metadata for the downloaded acquisitions will be stored.

</p>

<img width="100" height="30" src="https://github.com/LSFE/info/blob/master/example-3_figure-1.png"></a>


#### MODIS
<p align="justify">
</p>

</b>

Click <a href="https://github.com/LSFE/LSFE-R">here</a> to return to <i>LSFE</i> main page.
