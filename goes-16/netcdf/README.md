# GOES-16 NetCDF Access Test Notebook
 This test uses publically available GOES-16 data stored on the [Microsoft Planetary Computer Data Catalog](https://planetarycomputer.microsoft.com/catalog). 
 
 This notebook should be reproducible in any environment, but will work best on an Azure compute instance hosted in EU-West (where the data are stored). The method of access is using netcdf byte-range requests (appending `#mode=bytes` to the file's http url) and passing the list of urls to `xarray.open_mfdataset()`.