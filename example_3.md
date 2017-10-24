### Standardized storage of satellite data

<p align="justify">
One of the main issues in sharing data and tools between researchers has to do with the way we store and use data. Often, each researcher has its data structure which makes it hard to apply re-apply a tool. As a consequence, adapting the work of someone else might be a bigger effort than writting our own functions leading to an unnecessary replication of work.
To avoid this, we developed a series of tools to create a standized structure for satellite data and its corresponding metadata. Ideally, this function can be used in combination with <i>lsfeData()</i> (see <a href="https://github.com/LSFE/info/blob/master/example_3.md">here</a>).
</p>

#### Data structure
<p align="justify">
The data for every satellite sensor stored through <i>LSFE</i> will have a comparable structure. As describe in the disgram below, the storage functions will create a folder for the sensor within which two folders will be created:
  
* SR - Folder where the surface reflectance data will be stored.
* infos - Folder where per-tile metadata for the downloaded acquisitions will be stored.

Then, inside <i>SR</i>, the function will create a folder for each tile and store the corresponding acquisitions within it.
</p>

</b>

<p align="center">
<img width="709" height="371" src="https://github.com/LSFE/info/blob/master/example-3_figure-1.jpg"></a>
</p>

<p align="center">
<sub>Figure 1 - Example data storage diagram for Landsat.</sub>
</p>

</b>

<p align="justify">
 At the moment, <i>LSFE</i> offers the functions <i>storeLandsat()</i> and <i>store13Q1()</i> which help in the storage of  Landsat and MODIS 13Q1 data, respectively. As shown in the examples below, these functions only require that the user specifies the input path (where the downloaded data is stored) and the output folder (where the data will be sorted). Additionally, the user can choose to remove the original files after competion setting the keyword <i>remove.files</i> to <mark class="blue">TRUE</mark>.
</p>

```R
storeLandsat()
```


</b>

Click <a href="https://github.com/LSFE/LSFE-R">here</a> to return to <i>LSFE</i> main page.
