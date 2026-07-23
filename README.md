# Code for: "Spectral characterisation of short-wave infrared (SWIR) tissue chromophores and tissue-mimicking phantom optical properties"

**Authors:** [Melissa J. Watt](https://github.com/melissajanewatt), Layla Malouf, Ran Tao, Isabelle Racicot, Thomas R. Else, Janek Gröhl, Sarah E. Bohndiek. *University of Cambridge*

Contact details: Sarah E. Bohndiek, seb53@cam.ac.uk

Ths repository contains the code used for the paper "Spectral characterisation of short-wave infrared (SWIR) tissue chromophores and tissue-mimicking phantom optical properties" and associated dataset of SWIR tissue chromophore and tissue-mimicking phantom optical properties. The simulation dataset will be provided on Apollo - the University of Cambridge repository - upon acceptance.

## Python environment

This code has been written as Jupyter Notebooks (.ipynb) and requires a Python environment. The deposited version of the code was tested on Mac with Python 3.7.6.

## Code description

1. Directory "Data":

Contains 
    1) Directory "Download_Spectra": .txt and .npz files containing the absorption and reduced scattering cofficients we measured that can be readily downloaded. Note: the whole blood is horse blood, which has smaller RBC diameters than human RBCs, and thus the measured reduced scattering coefficient is lower than expected for human blood.
    2) Directory "RBCs": .csv files with horse red blood cell flow cytometry measured cell diameters.
    3) Directory "Reference Spectra": reference datasets of optical properties from literature (see paper for full description).
    4) Directory "Shmadzu": .csv files containing raw transmittance spectra measured with Shimadzu SIS system and a combined processed file with estimated absorption coefficient for all measured chromophores.
    5) Directory "Simulation_Spectra": optical properties used in SIMPA simulations. These data are a combination of spectra we measured and reference spectra from literature, see paper for details.
    6) Directory "in-house-SIS": conatins directories containing raw data and IAD outputs for each chromophore and tissue-mimicking phantom measured with the in-house SIS system and a combined processed csv file with estimated optical properties for all measured chromophores.
    7) Directory "po2_probe_data": raw data from oxygen probe.

2. Jupyter Notebook "Plots_for_Figures.ipynb": Code for generating figures and generating of models of whole blood scattering using Mie theory.

3. Jupyter Notebook "Post_process_IAD.ipynb": Code for postprocessing IAD algorithm outputs.

4. Jupyter Notebook "Process_spectra.ipynb": Code for estimating and processing absorption and reduced scattering coefficents of measured tissue chromophores and tissuue mimicking phantoms.

5. Jupyter Notebook "SIMPA_simulations.ipynb": Code for generating and simulating models of tissues and phantoms using the SIMPA python toolkit.

6. Jupyter Notebook "Simulation_analysis.ipynb": Code for calculating effective penetration depth from simulation results.

7. Jupyter Notebook "Statistical analysis.ipynb": Code for statistical comparison of our characterisations with reference data.

8. Jupyter Notebook "oxygenation analysis.ipynb": Code for calculating so2 using the Severinghaus equation from po2 measurements.

9. File "path_config.env": Path configuration file for SIMPA simulations.
