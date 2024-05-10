# Description

By using Autodock-GPU and Vdock, docking results are obtained for more than 5 million small molecules.

# Inputs
 ### Target : Protein Structure
 - Public : Can search for protein names.
   - Choose alphafold model or PDB structure
 - private : From the TARGETS menu, select the added protein.

 ### Binding Site : The center of the selected residues, where the molecules binding locate.
 - Site : Forecast in the Site app, Select the part that will be docked.
 - Residue : If you don't select Site, You can enter a residue number directly.

 ### Screening option : 
- Number of iteration : Number of iterations of retraining for docking and machine learning
- Initial screen data : The first docked data, a database clustered using similarity
  - NR10 : similarity < 10, approx. 6,000
  - NR15 : similarity < 15, approx. 35,000
  - NR20 : similarity < 20, approx. 140,000
- Screen data
  - Mcule purchasable : Mcule's instock compounds, approx. 5M
  - Enamine lead-like : Enamine's Real Diversity set, approx. 38.2M
- Docking number of data
  - Number of ligands docked per iteration (smaller takes less time, larger increases accuracy) 
- Lipinsk's rule of five : Filter conditions for screening molecules
  - Molecule Weight <= 500
  - Hydrogen bond donor <= 5
  - Hydroget bond acceptor <= 10
  - LogP <= 5.0 

 ### V-Dock option : 
 - Method : Select a machine learning kinds.
 - Feature : The feature type of the molecule to be used for machine learning.
# Outputs
## Web page
### Target
Explore the length and 3D structure of a protein structure.
### Seed docking
 - Binding energy distribution for initial screen data
 - The frequency and interaction type of the residues interacting with the molecule. 
### Result
It shows the structure of the molecule bound to the protein and the three binding energies (AK-Score2 Energy, Autodock Energy, and Autodock Cluster Energy).

## Download File
 - vdock_screening.dock.report.tsv : The resulting table contains UID, AK_E, BINDING_E, CLUSTER_E, and their respective RANK and CANON_SMILES.
 - vdock_screening.dock.AK_E : Structures for AK-Score2 for each molecule: a pdb file and an sdf file.
 - vdock_screening.dock.receptor.pdb : Protein structure file.
 - DOCK.report.pdf : Summary PDF file

# References

1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal
3. [Mcule database](https://mcule.com/database/)
4. [Enamine database](https://enamine.net/compound-collections/real-compounds/real-database-subsets)
