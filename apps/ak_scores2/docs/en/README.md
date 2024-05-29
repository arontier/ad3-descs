# Description

Calculates AK-Score2 energy given protein and compound structures.

---
# Inputs
 ### Target : Protein Structure
 - Public : Can search for protein names.
   - Choose alphafold model or PDB structure
 - private : From the TARGETS menu, select the added protein.

### Ligand : Compounds (pdb)
Insert a 3D structure file of the molecule that is binding to the protein.

   The pdb must include "CONECT" to ensure that the correct molecular bonds are represented.

---
# Outputs
## Web page
### Target
Explore the length and 3D structure of a protein structure.
### Result
It shows the structure of the molecule bound to the protein and its AK-Score2 Energy.

## Download File
 - AKscore.report.tsv : The resulting table contains UID, akscore2_nondock, akscore2_dock, akscore2_nondock_mul_dock, autodock_score, AK_E, AK_E_RANK, CANON_SMILES, INCHIKEY.
 - AKscore.AK_E : Structures for AK-Score2 for each molecule: a pdb file and an sdf file.
 - AKscore.receptor.pdb : Protein structure file.
 - failed_ligand.tsv : The name and reason for the molecule that AK-Score2 calculate failed.



---
# References
1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. AK-Score: Accurate Protein-Ligand Binding Affinity Prediction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
