# Testing cloud-optimized data files for L2 Satellite Data
This work was done as part of the National Center for Atmospheric Research (NCAR) Summer Internship in Parallel Computational Science (SIParCS)

This repo is a series of workflow tests for various cloud-hosted data access methods. Additional material, past presentations, posters, and interactive code tutorials are available here: https://lucassterzinger.com/2021-siparcs-poster/


# Test workflows
## GOES-16 Data:
* [Original NetCDF4](./goes-16/netcdf/)
* [Zarr](./goes-16/Zarr/)
* [ReferenceMaker (fsspec)](./goes-16/ReferenceMaker/)

Tests were performed on the [Microsoft Planetary Computer](https://planetarycomputer.microsoft.com/) with data hosted on Azure Blob object storage. Both Planetary Computer and the data used were performed in the EU-West region.

_More data for testing may be added in the future_

# Results
## GOES-16 24 hr data (144 files)
| Format           | Preprocess Time | Dataset Open Time | Workflow Time | Storage Needed |
|------------------|-----------------|-------------------|---------------|----------------|
| netCDF4 (native) | 0 min           | 10 min            | 46 min        | 0 GB           |
| Zarr             | 1 hr 38 min     | 30 sec            | 4 min 10 sec  | 416 MB         |
| RefereceMaker    | 1 hr 25 min     | 35 sec            | 4 min 30 sec  | 52 GB          |

# Contact me
Email: [lsterzinger@ucdavis.edu](mailto://lsterzinger@ucdavis.edu)

Twitter: [@lucassterzinger](https://twitter.com/lucassterzinger)
