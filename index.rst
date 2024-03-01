.. nbsphinx-rtd-test documentation master file, created by
   sphinx-quickstart on Wed Sep 28 16:20:38 2016.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


***This content is obsolete and will be deactivated or archived as of April 1, 2024.***

Welcome to a Collection of Tutorials for the Python Package `tobac`
===================================================================

.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Getting Started
   
   ./docs/RunningTutorials.md


.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Tracking for Beginners
   
   Test Blob in 2D <./tutorials/Basics/Idealized-Case-1_Tracking-of-a-Test-Blob-in-2D>
   Two crossing Blobs <./tutorials/Basics/Idealized-Case-2_Two_crossing_Blobs.ipynb>
   
   On Feature Detection: Part 1 <./tutorials/Basics/Methods-and-Parameters-for-Feature-Detection_Part_1.ipynb> 
   On Feature Detection: Part 2 <./tutorials/Basics/Methods-and-Parameters-for-Feature-Detection_Part_2.ipynb>
   On Segmentation <./tutorials/Basics/Methods-and-Parameters-for-Segmentation.ipynb>
   On Linking <./tutorials/Basics/Methods-and-Parameters-for-Linking.ipynb>  




.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Advanced Tracking: Observations
   
   OLR from GOES-13 Satellite <./tutorials/Example_OLR_Tracking_satellite/Example_OLR_Tracking_satellite>
   VIS from GOES-16 Satellite <./tutorials/Example_VIS_Tracking_Satellite/Example_VIS_Tracking_Satellite>


.. toctree::
   :maxdepth: 1 
   :hidden:
   :caption: Advanced Tracking: Simulations

   WRF OLR <./tutorials/Example_OLR_Tracking_model/Example_OLR_Tracking_model>
   WRF Precip <./tutorials/Example_Precip_Tracking/Example_Precip_Tracking>
   WRF Updrafts <./tutorials/Example_Updraft_Tracking/Example_Updraft_Tracking>
   WRF Mesoscale Vorticity <./tutorials/Example_vorticity_tracking_model/Example_vorticity_tracking_model> 


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
 * :doc:`Tracking of Observed OLR <./tutorials/Example_OLR_Tracking_satellite/Example_OLR_Tracking_satellite>`
 * :doc:`Tracking of Observed Visible Satellite Images <./tutorials/Example_VIS_Tracking_Satellite/Example_VIS_Tracking_Satellite>`
 * :doc:`Tracking of Simulated OLR <./tutorials/Example_OLR_Tracking_model/Example_OLR_Tracking_model>`
 * :doc:`Tracking of Simulated Precipitation Cells <./tutorials/Example_Precip_Tracking/Example_Precip_Tracking>`
 * :doc:`Tracking of Simulated Updrafts Cells <./tutorials/Example_Updraft_Tracking/Example_Updraft_Tracking>`
 * :doc:`Tracking of Simulated Vorticity Anomalies <./tutorials/Example_vorticity_tracking_model/Example_vorticity_tracking_model>`



* **your theme**
 *  We search for volunteers that included their cloud tracking or analysis approach into `tobac` as a new theme and provide nice tutorials on the cool new functions here.

