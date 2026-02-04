# Martini 3 Building Blocks for Lipid Nanoparticle Design
 
![Lipid Nanoparticle Components](LNP_components.png)

Welcome to the repository for **Martini 3 ionizable lipid parameters and protocols** tailored for the design and simulation of Lipid Nanoparticles (LNPs). These resources are designed to facilitate molecular dynamics simulations, enabling deeper insights into LNP formulation and function, particularly for pharmaceutical applications such as mRNA delivery.

## What’s Included
This repository provides:

1. **Ionizable Lipid Parameters:**  
   - Access the `Lipid_parameters` folder for ready-to-use Martini 3 parameters for:
      - Literature known Ionizable Lipids - `Lipid_parameters > Literature_known_lipids`;
      - Pre-built Ionizable Lipids - `Lipid_parameters > Ionizable_lipid_library`;
      - Ionizable Lipid Fragments - `Lipid_parameters > Fragments`.
      - Lipid parameters adapted according to [Pedersen et.al](ihttps://doi.org/10.1021/acscentsci.5c00755) - `Lipid_parameters > Refined_tail_Parameters`
   - Detailed descriptions on how to generate new lipid itps are provided in `Lipid_parameters > Scripts`.  

2. **Case Studies and Protocols:**  
   - Explore the `Case_studies` folder to obtain the protocols that guide you through:
      - Building Lipid Nanoparticles - `Case_studies > Lipid_Nanoparticle_construction`
      - Quantifying stalk formation - `Case_studies > Quantifying_stalk_formation`
      - Simulating Unbiased Fusion - `Case_studies > Unbiased_Fusion`   
       

## Citations
If you use the parameters/protocols from this repository, please cite the following publication:  
[Kjølbye, L. R., Valério, M., Paloncýová, M., Borges-Araújo, L., Pestana-Nobles, R., Grünewald, F., ... & Souza, P. C. (2024). Martini 3 building blocks for Lipid Nanoparticle design.](https://pubs.acs.org/doi/10.1021/acs.jctc.5c01207)


Please also cite the following packages/publications: 
| Protocol                             | Powered by                                                                               
|--------------------------------------|------------------------------------------------------------------
| Inverse Hexagonal core LNP  | [MDAnalysis](https://www.mdanalysis.org/); [Packmol](https://m3g.github.io/packmol/); [TS2CG](https://github.com/marrink-lab/TS2CG); [freud](https://freud.readthedocs.io/en/stable/gettingstarted/introduction.html); [mdvwhole](https://github.com/BartBruininks/mdvwhole); [mdvcontainment](https://github.com/BartBruininks/mdvcontainment/releases/tag/legacy)
| "Bleb" LNP                  | [MDAnalysis](https://www.mdanalysis.org/); [Packmol](https://m3g.github.io/packmol/); [TS2CG](https://github.com/marrink-lab/TS2CG); [freud](https://freud.readthedocs.io/en/stable/gettingstarted/introduction.html); [mdvwhole](https://github.com/BartBruininks/mdvwhole)
| Stalk Free Energy           | [Gromacs-chain-coordinate](https://gitlab.com/cbjh/gromacs-chain-coordinate); [insane.py](https://github.com/Tsjerk/Insane); [GROMACS](https://manual.gromacs.org/2024.1/install-guide/index.html)
