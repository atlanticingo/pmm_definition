# pmm_definition
This repository contains the NCL (https://www.ncl.ucar.edu/) code used for my analysis of interannual variability in the subtropical North Pacific.
Specifically, the project aims to critically reexamine the definition of the Pacific Meridional Mode (PMM), which is thought to dominate variability in the region.

Note that this repository only contains the code. It is meant to document how the analysis underlying the manuscript was performed. In order to reproduce the manuscript figures, several data sets will be needed. Specifically, skin temperature and 10m wind components from the NCEP/NCAR reanalysis and from the CMIP6 experiment piControl will be needed. These are freely available online. See here for the NCEP/NCAR reanalysis https://psl.noaa.gov/data/gridded/data.ncep.reanalysis.html, and here for the CMIP6 output https://esgf-node.llnl.gov/search/cmip6/. 

Following is a short description of the files.

analysis_code.ncl.v01.2022.03.10.tar
Contains various routines that were used during the analysis.

manuscript_figs_code.ncl.v01.2022.03.10.tar
Contains the code used to make the manuscript figures.

ncl.utils.2022.03.10.tar
Contains various utilities (subroutines) that are called from the other routines. These have to be loaded with load statement at the top of the individual routines. The environment variable $NCL_REPOS, which contains the path to the utilities, should set apprriately or replaced inline with the full path. If the utilities reside in the same directory as the analysis code, no path is needed.

etopo5.msk.0.25deg.nc
The land-sea mask used by the utility mask_fld.ncl, which is called by several routines.

basin_mask.nc
Basin mask (Pacific, Atlantic, etc.) used by the utility mask_basin.ncl, which is called by some routines.
