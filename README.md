# ukraine-energy-modelling

The Ukrainian energy system model is developed as an extension to the [PyPSA-Eur](https://github.com/PyPSA/pypsa-eur) model in this repository.

## Cloning the repository

The repository is structured to contain the PyPSA-Eur model as a submodule. All the modelling changes associated to the Ukrainian model itself will be developed in the main module.

There are two ways to clone the repository (1) Recursive cloning of the repository including the submodules or (2) Cloning the main and submodules independently

To recursively clone the modules, the flag `--recurse-submodules` is to be used along with the `git clone` command as follows:

    git clone --recurse-submodules git@github.com:instrat-pl/ukraine-energy-modelling.git

To independently clone the modules,

Firstly, the repository is cloned using the `git clone` command:

    git clone git@github.com:instrat-pl/ukraine-energy-modelling.git

and then using the `git submodule` command:

    git submodule update --init --recursive

The new commits of the submodule can be fetched and updated using the command:

    git submodule update --remote

## Input Data

The latest updated conventional powerplant data is provided as an input to the PyPSA-Eur model. This file needs to be copied from 
    
    Data/custom_powerplants.csv 

into the PyPSA-Eur model at the following location 
    
    workflow/pypsa-eur/Data/custom_powerplants.csv
    