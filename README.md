# Ancestral sequence reconstruction for biocatalytic stereoselective synthesis of azaphilones

This repo contains all the required data to replicate the molecular modelling of the acyltranferase ancestors.

## Install

Create the conda environment called anc_acyl

`conda env create -f environment.yml`

`conda activate anc_acyl`

Install [MMTSB Toolset](https://github.com/mmtsb/toolset)

Install [pyCHARMM](https://github.com/BrooksResearchGroup-UM/pyCHARMM-Workshop/tree/main/0Install_Tools)

In most scripts, the CHARMM_LIB_DIR is a required variable is the directory generated for pyCHARMM.

## Use

Each folder contains the data generated from modelling/docking and all the data necessary to reproduce our results.

Each folder (except [AlphaFold](https://github.com/google-deepmind/alphafold)), contains an **example** directory. The example directory contains an example script or notebook which should be run with the anc_acyl enviornment and the example directory as the current working directory. All generate output is placed in the output folder. See this folder for example output before running. Each example can be run independently with the provided data.

## Order

To reproduce the results from the paper, the following modelling order should be followed:

0. alphafold
1. vacuum_min
2. add_5cthioester
3. rcdocker
4. fcdocker
5. fcdocker_flexible_5cthioester
6. add_substrate
6. dyn
7. analysis