<!-- @format -->

# Description

Autodock-GPU to prediction the binding energy between proteins and molecules. \
Autodock4 and AK-Score2 are used as scoring methods.

# Inputs
 ### Target : Protein Structure
 - Public : Can search for protein names.
   - Choose alphafold model or PDB structure
 - private : From the TARGETS menu, select the added protein.

 ### Binding Site : The center of the selected residues, where the molecules binding locate.
 - Site : Forecast in the Site app, Select the part that will be docked.
 - Residue : If you don't select Site, You can enter a residue number directly.
   
### Ligand : 분자
 - Ligand : Put an SDF or PDB or MOL2 file.

   The pdb must include "CONECT" to ensure that the correct molecular bonds are represented.

# Outputs
## Web page
### Target
Explore the length and 3D structure of a protein structure.
### Result
It shows the structure of the molecule bound to the protein and the three binding energies (AK-Score2 Energy, Autodock Energy, and Autodock Cluster Energy).

## Download File
 - Dock.report.tsv : The resulting table contains UID, AK_E, BINDING_E, CLUSTER_E, and their respective RANK and CANON_SMILES.
 - Dock.AK_E : Structures for AK-Score2 for each molecule: a pdb file and an sdf file.
 - Dock.BINDING_E : Structures for autodock energy for each molecule: a pdb file and an sdf file.
 - Dock.CLUSTER_E : Structures for autodock cluster energy for each molecule: a pdb file and an sdf file.
 - Dock.receptor.pdb : Protein structure file.
 - failed_ligand.tsv : The name and reason for the molecule that docking failed.

# References
1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. AK-Score: Accurate Protein-Ligand Binding Affinity Prediction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
