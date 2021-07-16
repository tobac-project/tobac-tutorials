.. nbsphinx-rtd-test documentation master file, created by
   sphinx-quickstart on Wed Sep 28 16:20:38 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to a Collection of Tutorials for the Python Package `tobac`
===================================================================


.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Tracking in Observations
   
   ./tobac_v1/Example_OLR_Tracking_satellite/Example_OLR_Tracking_satellite


.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Tracking in Simulaitons

   ./tobac_v1/Example_OLR_Tracking_model/Example_OLR_Tracking_model
   ./tobac_v1/Example_Precip_Tracking/Example_Precip_Tracking
   ./tobac_v1/Example_Updraft_Tracking/Example_Updraft_Tracking



Intro
-----
This is a set of tutorial notebooks which provide example usage of the python package `tobac` - Tracking and Object-Based Analysis of Clouds.

The python package `tobac` is an open software for atmoshperic scientist aiming 
to support Lagrangian analysis of cloud fields. The methods can be applied either to observational fields or to simulated cloud variables.


Themes
------
The `tobac` package is structured in two layers: In the first layer, core functionality is provided. The second layer is called "themes" and provides a dedicated set of functions to track or analyse clouds. We keep separate developments in separate "theme" like plugins in your browser. Parts of the different themes might be exchangeable. 


Examples
---------

Examples or tutorial are collected to show how `tobac` and `tobac` "themes" are working. Function have been written to ease input of certain obervational or model-simulated fields available at TROPOS. These function included data from

* **tobac_v1**
 * :doc:`Tracking of Observed OLR <./tobac_v1/Example_OLR_Tracking_satellite/Example_OLR_Tracking_satellite>`
 * :doc:`Tracking of Simulated OLR <./tobac_v1/Example_OLR_Tracking_model/Example_OLR_Tracking_model>`
 * :doc:`Tracking of Simulated Precipitation Cells <./tobac_v1/Example_Precip_Tracking/Example_Precip_Tracking>`
 * :doc:`Tracking of Simulated Updrafts Cells <./tobac_v1/Example_Updraft_Tracking/Example_Updraft_Tracking>`


* **your theme**
 *  We search for volunteers that included their cloud tracking or analysis approach into `tobac` as a new theme and provide nice tutorials on the cool new functions here.
