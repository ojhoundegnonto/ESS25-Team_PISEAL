# Physical Processes Impacting Regional Sea Level (PISeaL)

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

## Files and folders in your project repository

This template provides the following suggested organizaiton structure for the project repository, but each project team is free to organize their repository as they see fit.

* **`contributors/`**
<br> Each team member can create their own folder under contributors, within which they can work on their own scripts, notebooks, and other files. Having a dedicated folder for each person helps to prevent conflicts when merging with the main branch. This is a good place for team members to start off exploring data and methods for the project.
* **`notebooks/`**
<br> Notebooks that are considered delivered results for the project should go in here.
* **`scripts/`**
<br> Code that is shared by the team should go in here (e.g. functions or subroutines). These will be files other than Jupyter Notebooks such as Python scripts (.py).
* `.gitignore`
<br> This file sets the files that will be globally ignored by `git` for the project. (e.g. you may want git to ignore temporary files or large data files, [read more about ignoring files here](https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files))
* `environment.yml`
<br> `conda` environment description needed to run this project.
* `README.md`
<br> Description of the project (see suggested headings below)
* `model-card.md`
<br> Description (following a metadata standard) of any machine learning models used in the project

# Project or Team Name

### Team members

List all participants on the project. Here is a good space to share your personal goals for the hackweek and things you can help with.

| Name | Personal goals | Can help with | Role |
| ------------- | ------------- | ------------- | ------------- |
| Yueyang Lu | learn how to use python to work with ocean model data  | sea level dynamics, MATLAB  | Project Lead |
| Odilon J. Houndegnonto| Practice leading a software project | machine learning and python (scipy, scikit-learn) | Project Lead |
<!--| Alan T. | learning about your dataset | GitHub, Jupyter, cloud computing | Project Helper |-->
<!--| Rachel C. | learn to use github, resolve merge conflicts | I am familiar with our dataset | Team Member  |-->
<!--| ... | ... | ... | ... |-->
<!--| ... | ... | ... | ... |-->

### The problem

Provide a few sentences describing the problem are you going to explore. If this is a technical exploration of software or data science methods, explain why this work is important in a broader context and specific applications of this work.

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




