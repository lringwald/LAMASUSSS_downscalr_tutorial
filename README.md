Here is a summary tailored to serve as a README or description for your GitHub repository:

# LAMASUSSS Land-Use Downscaling Tutorial with `downscalr`

### About This Repository

This repository provides a comprehensive, hands-on tutorial and the accompanying data files for downscaling aggregate land-use (LU) and land-use change (LUC) projections from Integrated Assessment Models (IAMs), such as GLOBIOM, to high-resolution spatial grids.

Through progressive examples, this guide walks you through the spatial allocation of land-use targets, starting from basic, conceptual allocation rules and culminating in the advanced econometric routines provided by the `downscalr` R package.

---

### What You'll Learn

* **Core Concepts:** Understand the essential ingredients of spatial downscaling:
* **LUC Targets:** The aggregate land-use change quantities (e.g., country-level transitions).
* **Start Maps:** High-resolution spatial templates of initial land-use states (e.g., 10x10km Corine Land Cover grids).
* **Allocation Methods:** The rules governing how aggregate targets are distributed across the high-resolution grid.


* **Basic Approaches:** Explore introductory techniques to build intuition, ranging from a "naive" uniform distribution to conditional and proportional pixel-share downscaling.
* **The `downscalr` Framework:** Master the full downscaling workflow bridging observed drivers and aggregate targets:
* **Prior Module:** Estimate spatial transition probabilities using an empirical Bayesian Multinomial Logistic (MNL) regression model.
* **Downscale Module:** Precisely allocate targets across the map using bias correction, guided by your estimated priors and high-resolution start maps.



---

### Repository Features & Code Examples

The included scripts and data sets will allow you to replicate the tutorial and adapt the workflow for your own research. Key examples include:

* **Data Wrangling & Mapping:** Learn to aggregate raw land cover data, map spatial resolutions, align thematic classifications to fit GLOBIOM/UNFCCC standards, and visualize results using `ggplot2`.
* **Multi-Class & Multi-Step Projections:** Expand the MNL estimation and downscaling routines to handle multiple origin/destination LU classes simultaneously across rolling future time steps (e.g., 2010 to 2100).
* **Spatial Restrictions:** Inject exogenous policy or geographic constraints into the model, such as blocking transitions in protected *Natura 2000* conservation areas.
* **Exogenous Priors:** Learn how to handle transitions for novel land-use types (e.g., Short Rotation Plantations) that lack historical observational data by introducing exogenous prior probabilities.

---

### Prerequisites

To run the examples in this repository, you should be comfortable with R and spatial data manipulation. Make sure you have the following packages installed:

* `downscalr`
* `dplyr`
* `tidyr`
* `ggplot2`
* `reshape2`
