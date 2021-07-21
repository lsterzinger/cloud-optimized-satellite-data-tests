# GOES-16 Zarr Access Test Notebook
 This test uses publically available GOES-16 data stored on the [Microsoft Planetary Computer Data Catalog](https://planetarycomputer.microsoft.com/catalog). 
 
 This notebook will not be reproducible as it relies on a private object storage account on Azure. The code could easily be modified to support a different connection string/storage host/account.

 The data are pulled in via NetCDF byte-range mode (Same as [../netcdf/](../netcdf/)). `xarray.Dataset.to_zarr()` is then used to write the data as Zarr directly to Azure Blob storage.