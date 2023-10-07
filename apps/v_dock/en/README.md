# Description 

We propose a computational workflow to design novel drug-like molecules by combining the global optimization of molecular properties and protein-ligand docking with machine learning. However, most existing methods depend heavily on experimental data, and many targets do not have sufficient data to train reliable activity prediction models. To overcome this limitation, protein-ligand docking calculations must be performed using the limited data available. Such docking calculations during molecular generation require considerable computational time, preventing extensive exploration of the chemical space. To address this problem, we trained a machine-learning-based model that predicted the docking energy using SMILES to accelerate the molecular generation process. Docking scores could be accurately predicted using only a SMILES string. We combined this docking score prediction model with the global molecular property optimization approach, MolFinder, to find novel molecules exhibiting the desired properties with high values of predicted docking scores. We named this design approach V-dock. Using V-dock, we efficiently generated many novel molecules with high docking scores for a target protein, a similarity to the reference molecule, and desirable drug-like and bespoke properties, such as QED. The predicted docking scores of the generated molecules were verified by correlating them with the actual docking scores

# Inputs

# Outputs


# References

* Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal

