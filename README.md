# Python Basic Spatial Analysis
This Python script makes use of several spatial packages (such as geopandas) to conduct a basic CAFO analysis count of all counties in North Carolina using NC spatial data. The finalData.csv file was produced from the CAFO-Analysis project (repository available), which used R instead of Python.

## IMPORTANT!!!
This particular notebook uses the package "geopandas" among others; part of this library installation process includes installing "fiona". 
I personally ran into an issue with importing "geopandas" because of conflicting dependencies from different Anaconda channels. 
Here is the error message from my Python notebook:

```
ImportError: dlopen(/Applications/anaconda3/lib/python3.6/site-packages/fiona/ogrext.cpython-36m-darwin.so, 2): Library not loaded: @rpath/libpoppler.71.dylib
  Referenced from: /Applications/anaconda3/lib/libgdal.20.dylib
  Reason: image not found
```

Here is the bash code that I used to address that issue in case you run into it:
  
```
conda install fiona pyproj six
pip install geopandas
```

## Data
You can find the spatial data set of the counties and state borders of North Carolina here: 
https://hub.arcgis.com/datasets/34acbf4a26784f189c9528c1cf317193_0/data

finalData.csv was produced with the scripts from (and can accordingly also be found at) the CAFO-Analysis project repository in the derivedData folder:
https://github.com/tedcwang/CAFO-Analysis
