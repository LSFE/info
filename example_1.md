### A uniform workspace

<p align="justify">
In order to facilitate the exchange of tools for data processing and analysis we developed <i>lsfeData()</i>. Provided a target directory, this fuction will generate a consistent workspace locally structure as:

* <b>00_DATA</b> - Base and/or processed satellite data stored by tiles (see xxxx).
* <b>01_RESULTS</b> - Processed satellite data (e.g. subsets for test site) and/or scientific analysis outputs.
* <b>02_DOCUMENTS</b> - General documentation.
* <b>03_CODE</b> - Scripts (R or other).
* <b>04_SANDBOX</b> - Folder dedicated to data testing which is independent from the remaining data structure.

</p>



```R
install.packages("devtools")
require(devtools)
```
