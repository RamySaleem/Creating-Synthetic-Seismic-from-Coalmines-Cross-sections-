**Synthetic Seismic Modelling of Geological Interpretations**
==============================================
**Using Coalmines Subsurface Cross-sections from**
=========================================
**Ruhr Sub Basin, Lower Rhine Basin, Germany**
======================================

![Synthetic Seismic Section](https://i.imgur.com/xFOw79c.png)

Introduction
==========
Seismic data provide a “time picture” of subsurface structure. 2D reflection seismic data provide cross-sectional views in both the dip and strike directions. Data on the lines are a mixture of both in-plane and out-of-plane reflectors. 2D reflection seismic data are most important in the earlier stages of an exploration program, especially in frontier basins.

Seismic imaging is the key method for imaging the structure of the subsurface. Data are generated by sending acoustic energy (sound waves) into the Earth and recording the reflections which are returned from the various layers. Seismic imaging is used extensively in the petroleum industry and also in mining, civil engineering and hydro-geology.
https://wiki.aapg.org/Seismic_data

Synthetic Seismic Data
===================
Synthetic seismic data is artificial data generated using forward modelling to replicate the subsurface geological structures. We use interpreted geological cross-sections to generate the synthetic data in this case.
https://wiki.aapg.org/Synthetic_seismogram

Aims
====
The aims of this project are:

1.	Develop a python code to generate synthetic seismic data from vector images.
2.	Produce a suite of synthetic seismic sections from coalmines data in the Ruhr subbasin, lower Rhine basin, Germany.

Methods
=======
1.	Build the stratigraphic model of the area.
2.	Get the lithology of each cross-section from the stratigraphic model
3.	Select average stander velocities and densities for each lithology
4.	Calculate the acoustic impedance by multiplying the density of the rocks by the velocity of the rocks (vp * rho)
5.	Calculate reflection coefficients, Ro. The reflection coefficient is the acoustic impedance of the upper layer subtracted from the lower layer divided by the sum of the two. 
6.	Convolve the reflection coefficient series with the Ricker wavelet.

![image.png](https://wikimedia.org/api/rest_v1/media/math/render/svg/4243db6b3dab87b7be571c98f8f7568824ad4a6a)


Ruhr Coalmines DataSet
=====================
**Area-1 Summary**

The study area is explored by high-resolution, closely spaced, coal mines with an aerial extent of 323.29 km2 and a depth of 2 km. The subsurface data are provided by mine-workings (galleries, adits and shafts) as well as accompanying boreholes and seismic reflection profiles, which are supported by surface exposure enhanced by open-cast pits. These data were interpreted by Drozdzewski et al. (1980), who reported these observations and erected their own geological interpretations on a series of paper maps and cross-sections. 

They are a set of 12 serial cross-sections with a spacing of 1 to 2 km and tied by two cross-lines. Further, Drozdzewski et al. (1980) indicate the levels of confidence in their interpretations critically using descriptive criteria. The stratigraphic column present in this study is put together and generated after Drozdzewski et al. (1980), Drozdzewski (1993), Suess et al. (2007), Cleal et al. (2009) and Uhl and Cleal (2010). The lithology, formations names, coal seams and stratigraphic units in this stratigraphic column are constrained by correlating the stratigraphic units from Drozdzewski et al. (1980) to other recent studies (e.g. Cleal et al. 2009; Uhl and Cleal 2010). 

**Dataset can be found in the following links:**
1. **Interpreted Images** https://drive.google.com/drive/folders/1j4PBXQyVx89rkVTvMS7Yjl7e7y5OTDrC?usp=sharing
2. **Digitised Cross Sections** https://drive.google.com/drive/folders/1EabQCWqC1JExdLTRCJRx8MDAGHAhHy5N?usp=sharing
3. All the maps and cross-section of the Ruhr subbasin, lower Rhine basin is available in the North Rhine-Westphalia Geological Survey – State Office – (GD NRW) for a fee https://www.gd.nrw.de/pr_kd.htm
4. All the CSV files used in this study https://drive.google.com/drive/folders/14f8_Hzbos23ww6Do96CO2KGeDIIE870h?usp=sharing



Results
======
1. Generate an ML dataset for testing subsurface interpretations
2. Generate a dataset of synthetic seismic images which can be used for educational peruses
3. Develop workflows for building synthetic seismic sections
4. Generate a dataset to develop ML Workflow for efficient classification of structures using object detection
5. Compare actual and synthetic seismic data from coalmines data in the Ruhr subbasin, lower Rhine basin, Germany.

**Results images can be found in the following links:**
1. **Acoustic Impedance Sections** https://drive.google.com/drive/folders/1ANce0auhTOXS0lcIoMfbTcG2r4lTdgfX?usp=sharing
2. **Synthetic Seismic Sections** https://drive.google.com/drive/folders/1C6TAHjFPzltrU4nS1oeHeEdBsEVkWzDM?usp=sharing

Future work
===========
To develop a workflow and web-based front end for the script, which will allow the rapid upload of geological data into the forward seismic modelling to generate synthetic seismic data.

Acknowledgements 
=================
The work contained in this repositories contains work conducted during a PhD study undertaken as part of the Natural Environment Research Council (NERC) Centre for Doctoral Training (CDT) in Oil & Gas funded 50% through its National Productivity Investment Fund grant number NE/R01051X/1 and 50% by the University of Aberdeen through its PhD Scholarship Scheme. The support of both organisations is gratefully acknowledged. The work is reliant on Open-Source Python Libraries, particularly numpy, OpenCV, cv2 matplotlib, bruges and pandas and contributors to these are thanked, along with Jovian and GitHub for open access hosting of the Python scripts for the study.

![University of Aberdeen](https://i.imgur.com/PILyj4m.jpg)

![NERC-CDT](https://nerc-cdt-oil-and-gas.ac.uk/wp-content/uploads/news/2015-news-NERC-funding.jpg)

![NERC](https://auracdt.hull.ac.uk/wp-content/uploads/2019/11/UKRI_NER_Council-Logo_Horiz-RGB.png)

![CDT](https://i.imgur.com/QDOhcN3.png)


