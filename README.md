# M3-Ionizable-Lipids

## Collection_of_itps
This folder contains a collection of pre-made parameters of ionizable lipids (ILs).
Within this folder are the folders:

> Literature_known_ILs 

> Ionizable_lipids_auto_itps_[name]

In the folder Literature_known_ILs are itps for commenly used and recognized ILs in the literature. 

The folders ionizable_lipids_auto_itps_[name] contains the collection of itps for one type of ILs with a veriation in the tails, in terms of lenght and saturation. 
These itps are generated using the script generate-from-table-v02.py which uses the script lipid-itp-generator-Martini3-01-ILs_simplified_ver1.py. 
In simple terms, it reads the .csv files, containing the lipid names and definitions, and then generates the itps from that.  

There are two python scripts for generating the parameters as well alng with corresponding csv files with information.


## Fragments

This folder contains folders for each fragment, which their corresponding itp (neutral/charge) and plots of the bonded distributions along with SASA. 
Hence if you need a new special made lipid, you can take the needed parameters from these fragments. 

## Notebooks
Herein you find useful notebooks for constructing and analyszing systems used in the paper.
> First off you can find the notebooks used for setting up and analyzing different membrane patches

> Secondly, notebooks for constructing a LNP with inverse hexagonal core can be found here: https://github.com/Martini-Force-Field-Initiative/M3-Ionizable-Lipids/tree/main/Notebooks/Inverse_Hexagonal_core_LNP
Input files for the three LNPs simulated in the paper can also be found in this folder. 

