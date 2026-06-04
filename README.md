# Supplementary Data Codes

**Correlation between nanoscale spatial heterogeneity and primary crystallization in amorphous Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> materials**

Huang Huang<sup>1</sup>, Jiong Zhou<sup>1</sup>, Junhan Hou<sup>1</sup>, Xi Yang<sup>1</sup>,  Huipu Liu<sup>1</sup>, Fan Zhu<sup>1*</sup>    

<sup>1</sup>College of Smart Materials and Future Energy, Fudan University, Shanghai 200438, China    
**Correspondence and requests for materials should be addressed to corresponding author (fzhu@fudan.edu.cn).*     


## Contents

- [Overview](#overview)
- [System Requirements](#system-requirements)
- [Repositary Contents](#repositary-contents)

# Overview

Spatial heterogeneity is an intrinsic structural characteristic of amorphous materials and has been shown to be closely linked to numerous physical properties. However, its correlation with crystallization behaviors, particularly in phase-change materials, remains poorly understood. Here, we systematically investigate the spatial heterogeneity and medium-range order (MRO) in amorphous Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> (GST) materials using high-angle annular dark-field scanning transmission electron microscopy (HAADF-STEM)，differential scanning calorimetry (DSC) and atomic electron tomography (AET). We reveal that the correlation length of spatial heterogeneity increases progressively with sub-glass transition temperature (sub-Tg) annealing time, accompanied by the growth and interconnection of crystal-like MRO networks. Concurrently, the crystallization activation energy decreases markedly. Our findings reveal a relationship between MRO-associated enhancement spatial heterogeneity and the reduced kinetic barrier to primary crystallization, offering a promising route to optimize phase-change memory performance via precisely controlled thermal annealing protocols.

# System Requirements

## Hardware Requirements

We recommend a computer with 16G DRAM, standard i7 4-core CPU, and a GPU to run most data analysis source codes. But for the 3D reconstruction of the experimental data with RESIRE, atomic tracing and refinement, we recommend a computer with large memory (512G DRAM, 16-core CPU and 1 GPU).

## Software Requirements

### OS Requirements

This package has been tested on the following Operating System:

Linux: Ubuntu 22.04.5 LTS  
Windows: Windows 11, version 23H2  
Mac OSX: We have not tested it on a Mac yet, but it should in principle work.

### Matlab Version Requirements

This package has been tested with `Matlab` R2021b. All the codes have to run in their own folders. We recommend the use of `Matlab` version R2021a or higher to test the data and source codes.

# Repositary Contents

### 1. Experiment Data

Folder: [1_Measured_data](./1_Measured_data)

This folder contains experimental images after denoising and alignment as well as their corresponding tilt angles for the amorphous Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> nanoparticles.

### 2. The REal Space Iterative REconstruction (RESIRE) Package

Folder: [2_RESIRE_package](./2_RESIRE_package)

Run the code `Main_RESIRE_as_dep_GST.m`,`Main_RESIRE_anneal_30min_GST.m`,`Main_RESIRE_anneal_60min_GST.m` to achieve the 3D reconstruction of the three Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> nanoparticles.

### 3. Reconstructed 3D Volume

Folder: [3_Final_reconstruction_volume](./3_Final_reconstruction_volume)

This folder includes the 3D reconstructed volumes of the three Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> nanoparticles.

### 4. Atom Tracing

Folder: [4_Atom_tracing](./4_Atom_tracing)

Run the codes `Main_atom_tracing_as_dep_GST.m`, `Main_atom_tracing_anneal_30min_GST.m` and `Main_atom_tracing_anneal_60min_GST.m` to trace the candidate atomic positions from the reconstructed 3D volumes.

Run the codes `Main_remove_non_atom_peak_as_dep_GST.m`, `Main_remove_non_atom_peak_aanneal_30min_GST.m` and `Main_remove_non_atom_peak_aanneal_60min_GST.m` to distinguish non-atoms from the candidate atoms via the K-mean clustering method. Through carefully comparison between the individual atomic positions in the candidate atomic models and the 3D reconstructions, a small fraction of unidentified or misidentified atoms were manually corrected, producing the 3D atomic models of the three Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> nanoparticles.

### 5. Experimental Atomic Model

Folder: [5_Final_coordinates](./5_Final_coordinates)

This folder includes the final 3D atomic models of the three Ge<sub>2</sub>Sb<sub>2</sub>Te<sub>5</sub> nanoparticles.

### 6. Post Data Analysis

Folder: [6_Data_analysis](./6_Data_analysis)

Run the codes `RDF_as_dep_GST.m`, `RDF_anneal_30min_GST.m` and `RDF_anneal_60min_GST.m` to calculate the radial distribution functions for all the atoms in the three amorphous materials.