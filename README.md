# HER-with-PGMs
This is the repository of the work "Toward Controllable and Predictable Synthesis of High-Entropy-Alloy Nanocrystals," containing the inputs and outputs of VASP computations. The results are summarized in **Figure 1**.

![image](https://user-images.githubusercontent.com/72870425/222903421-cdb26a69-35e3-4fc1-80e0-ce7713f48a6e.png)
**Figure 1.** The $\Delta G_{H^*}$ distribution of ~200 H-adsorbate configurations of 4 different types of slabs. The computational details can be found in the Supporting Information of the main article.

## Computational workflow 
The flowchart of our computations is summarized in **Figure 2**. A 3x3 5-layer (111) slab created from fcc crystal (a = 2.3 Å for primitive cell, vacuum layer = 15 Å) was constructed first, which was followed by random assignment of element on each lattice point.

![image](https://user-images.githubusercontent.com/72870425/222904004-3fca3996-bc9a-4549-8d34-15cdfff8197c.png)
**Figure 2.** The flowchart of surface structure construction. The “1NN” stands for “the first nearest neighbor on the top layer.

## INPUTS
This folder contains input files for geometry optimization (**optimization/**) and molecular dynamics dimulations (**MD/**) computations by VASP.
In **optimization** folder, there are INCAR and KPOINTS.
In **MD** folder, there are four subfolders and there are INCAR and KPOINTS in each subfolder. The heating process is summarized in **Figure 3.**
```
a. Heating up to 6000K (heating_to_6000/)  
b. Equilibration at 6000K (equil_at_6000/)   
c. Cooling down to 300K (cooling_to_300/)
d. Equilibration at 300K (equil_at_300/)   
```
![image](https://user-images.githubusercontent.com/72870425/222903797-299df748-d22f-48cb-b8e0-7b9a60b2bf69.png)
**Figure 3.** The thermal process of the “melt & quench” procedure. Three disordered slabs are constructed by quenching at different time steps from 6000 K to 300 K.

## OUTPUTS
This folder contains the H-adsorption free energy in eV and json format (deltaGH.json) and stuctures (CONTCAR) of all slabs (with and without H adsorption) considered in this work. For the nomenclature, please refer to the supporting information of the work. Threre are four different types of slabs:
```
a. Smooth primitive (smooth_primitive)
b. Smooth vacancy (smooth_vacancy)
c. Smooth step (smooth_step)
d. Disordered (amorphous)
```
In each folder, there are two subfolders:
```
a. Slab without H adsorbate (wo_H)
b. Slab with H adsorbate (w_H)
```
