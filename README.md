# Optimizing Hybrid Models for Canopy Nitrogen Mapping from Sentinel-2 in Google Earth Engine

## Abstract

Canopy nitrogen content (CNC) is a crucial variable for plant health, influencing photosynthesis and growth. An optimized, scalable approach for spatially explicit CNC quantification using Sentinel-2 (S2) data is presented, integrating PROSAIL-PRO simulations with Gaussian Process Regression (GPR) and an Active Learning technique, specifically the Euclidean distance-based diversity (EBD) approach for selective sampling. This hybrid method enhances training dataset efficiency and optimizes CNC models for practical applications.
Two GPR models based on PROSAIL-PRO variables were evaluated: a protein-based model (Cprot-LAI) and a chlorophyll-based model (Cab-LAI). Both models, implemented in Google Earth Engine (GEE), demonstrated strong performance and outperformed other machine learning methods, including kernel ridge regression, principal component regression, neural network, weighted k-nearest neighbours regression, partial least squares regression and least squares linear regression. 

## Use

In order to run the code in for example Anaconda JupyterLab, you will need a Google Earth Engine account and create an ImageCollection asset. When running the main notebook, you will have to connect to your own GEE account. Make sure to copy your ImageCollection path into the script (including a closing / at the end). You can adjust the region and time frame of interest to your own liking. Once the maps are exported to your GEE assets, you can download them into your Google drive. The images include two bands: the first one has the CNC estimates and the seconds the model's epistemic uncertainty.

The models can also be run directly in GEE, although results only include estimates and no uncertainties, due to high computational costs. The models and example script can be accessed on: https://code.earthengine.google.com/?accept_repo=users/declerckemma/S2-EBD-GPR-CNC.
