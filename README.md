# Physical Processes Impacting Regional Sea Level (PISeaL)
## Files and folders in this project repository

The organizaiton structure for this project repository is as follow:

* **`contributors/`**
<br> Contains each team member work on their own scripts, notebooks, and other files.
* **`notebooks/`**
<br> All Jupyter notebooks generated for this project are included here. Here, are all scripts that all team member work on together.
* `.gitignore`
<br> This file sets the files that will be globally ignored by git for the project. (e.g. you may want git to ignore temporary files or large data files, read more about ignoring files [here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files))
* `environment.yml`
<br> `conda` environment description needed to run this project.
* `README.md`
<br> Description of the project (see below)

### Team members

<div align="center">
<img src="figures/ECCO2025_PiSeal_YL_and_OJH.PNG" height="450" alt="PiSeal Team photo"  />
</div>

From left to right: [Odilon J. Houndegnonto](https://ojhoundegnonto.github.io) (from NASA-JPL/Caltech) and [Yueyang Lu](https://yueyanglu.github.io/) (from COAPS/FSU).


List all participants on the project. Here is a good space to share your personal goals for the hackweek and things you can help with.

| Name | Personal goals | Can help with |
| ------------- | ------------- | ------------- |
| Yueyang Lu | learn how to use python to work with ocean model data  | sea level dynamics, MATLAB  | 
| Odilon J. Houndegnonto| Strengthen my skills with ECCO products—including their strengths, limitations, access, implementation, and configuration (e.g. work from tile format to regular latlon format) | Ocean Physics, Python and MATLAB | 


## Project summary 
<div align="justify">
The primary objective of this analysis is to derive and examine the sea level budget using the ECCO (Estimating the Circulation and Climate of the Ocean) model version 4 release 5 (v4r5), with a particular focus on understanding the processes—specifically manometric (mass-related) and steric (density-related) effects—that influence regional sea level changes along the U.S. East Coast. To accomplish this, several key oceanographic fields are utilized, including sea surface height (SSH), density, volume fluxes, and surface freshwater and salt fluxes, among others. By leveraging these tools and datasets, the analysis aims to clarify how different physical processes contribute to observed variations in regional sea level, enhancing our understanding of both natural variability and potential future changes.
</div>

## Motivation
Global sea level has been rising at approximately 4.5 mm per year in the 21st century, which is about twice as fast as the rate observed during the 20th century ([Hamlington et al. 2024](https://www.nature.com/articles/s43247-024-01761-5)). However, this rise is not spatially uniform; different regions are dominated by different processes, leading to significant variations in the rate and causes of sea level change around the world.

## Scientific questions
- What physical processes influence sea level changes in different regions?
- What are their relative importance?

## Approaches
Sea Level = manometric & steric components ([Piecuch et al. 2019](https://doi.org/10.1029/2019JC015339)):

# $\eta = \eta_m + \eta_s = \frac{p_b}{\rho_0 g} - \frac{1}{\rho_0}\frac{H+\eta}{H}\int_{-H}^0{\rho'}dz^* $

Steric = thermosteric & halosteric components:

# $\eta_{s-T} = - \frac{1}{\rho_0}\frac{H+\eta}{H}\int_{-H}^0{ [\rho(S_r,T,p) - \rho(S_r,T_r,p)] }dz^* $ 
# $\eta_{s-S} = - \frac{1}{\rho_0}\frac{H+\eta}{H}\int_{-H}^0{ [\rho(S,T_r,p) - \rho(S_r,T_r,p)] }dz^* $


## Data and Resources

ECCOv4r5 dataset files used:

- OCEAN_TEMPERATURE_SALINITY_mon_mean_native_llc090_ECCOV4r5
- OCEAN_DENS_STRAT_PRESS_mon_mean_native_llc090_ECCOV4r5
- OCEAN_BOTTOM_PRESSURE_mon_mean_native_llc090_ECCOV4r5
- SEA_SURFACE_HEIGHT_mon_mean_native_llc090_ECCOV4r5
- ECCO_L4_GEOMETRY_LLC0090GRID_V4R4

We also used ECCO tutorial: https://ecco-v4-python-tutorial.readthedocs.io/ 

## Project Results

ECCO’s dynamical sea surface height can be decomposed into manometric (mass-related) and steric (density-related) components across most of the global oceans. In shelf regions, mass changes tend to play a more significant role, whereas in the open ocean, density changes are generally dominant. Within the steric component, thermosteric effects (temperature-related) are typically more influential than halosteric effects (salinity-related). There are notable regional differences in the effects of these components: over the European shelf, the manometric component ($\eta_m$) is the primary driver of total sea level variability, while in the eastern tropical Atlantic, particularly the Gulf of Guinea, the steric component ($\eta_s$) dominates total sea level variability, with $\eta_m$ contributing mainly to long-term trends.


Our final powerpoint slide can be found here: [FINAL PROJECT SLIDE](https://drive.google.com/file/d/1nhWoUrIOIigZVH29XEUw1yShPFtxQBmy/view?usp=sharing)


