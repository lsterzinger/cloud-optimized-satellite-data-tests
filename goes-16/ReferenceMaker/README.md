# GOES-16 ReferenceMaker Access Test Notebook
 This test uses publically available GOES-16 data stored on the [Microsoft Planetary Computer Data Catalog](https://planetarycomputer.microsoft.com/catalog). 
 
 This notebook should be reproducible in any environment, but will work best on an Azure compute instance hosted in EU-West (where the data are stored). 
 
 The method of access is using fsspec's [ReferenceMaker](https://github.com/intake/fsspec-reference-maker). The method creates metadata reference JSON files either locally or to cloud storage. These references can then be utilized to open the NetCDF4 file as a Zarr with `xarray.open_dataset(./path/to/json, engne='zarr')`. For more information, please see [this blog post I wrote as a tutorial](https://medium.com/pangeo/fake-it-until-you-make-it-reading-goes-netcdf4-data-on-aws-s3-as-zarr-for-rapid-data-access-61e33f8fe685) and its [corresponding repository](https://github.com/lsterzinger/fsspec-reference-maker-tutorial).