# Description

### Reverse docking
A method of prediction binding energy by docking a compound to multiple proteins. \
It can identify proteins that potentially bind to a compound, or it can be used to learn about the toxicity of a drug.

### Fittest
 A method for finding common or simultaneously targeted proteins for multiple compounds. \
For each compound, the score of bound proteins is normalized to a Z-score, and the Z-scores are summed to find the most likely proteins to bind to the ligands. 

### Database
 Protein structures were imported from three databases (RCSB PDB, AlphFold DB, and Uniprot). \
 The known binding sites were organized by PLIP and calculated for the protein structure with three binding site prediction programs (P2Rank, Fpocket, DeeSurf). \
 Finally, we clustered the binding sites to create a protein structure and binding site database. 
![image](https://github.com/arontier/ad3-descs/assets/98073046/dc7cad49-3733-4bc1-885b-4c7af2439b2b)


### Method
* Docking : Autodock-GPU
* Scoreing : AK-Score2, Z-score

---------------------
# Inputs
### Ligands
 - Ligands : sdf or pdb file.

   The pdb must include CONECT to ensure that the correct molecular bonds are represented.
### Similar ligand
Find compounds in the ZINC20 Database that have a similarity of 0.8 or higher and add them until the number of ligands reaches 10 (it may not be 10).

---------------------
# Outputs
## Web page
### Target
 Molecule Weight (MW), logP, Hydrogen bond donor (HBD), Hydrogen bond acceptor (HBA), TPSA, QED, SMILES, 2D image of Compounds.

### Target analyze

 - Plotted a heatmap of the correlation between Autodock energy and AK-Score2 energy of proteins across compounds.
 - The relationship between compounds is represented as a Diversity tree.

### Protein Candidates 
It shows the structure of the top proteins and molecules based on their Z-Score Energy and AK-Score2 Energy.


## Download File
 - vdock_screening.dock.report.tsv : The resulting table contains UID, AK_E, BINDING_E, CLUSTER_E, and their respective RANK and CANON_SMILES.
 - vdock_screening.dock.AK_E : There are two structures for AK-Score2 for each molecule: a pdb file and an sdf file.
 - vdock_screening.dock.receptor.pdb : Protein structure file
 - DOCK.report.pdf : Summary PDF file
 
---------------------

# References
1. H.M. Berman, J. Westbrook, Z. Feng, G. Gilliland, T.N. Bhat, H. Weissig, I.N. Shindyalov, P.E. Bourne, The Protein Data Bank (2000) Nucleic Acids Research 28: 235-242
2. Varadi, M. et al. “AlphaFold Protein Structure Database in 2024: Providing structure coverage for over 214 million protein sequences.” Nucleic Acids Research, gkad1011 (2023).
3. UniProt: the Universal Protein Knowledgebase in 2023. Nucleic Acids Res. 51:D523–D531 (2023)
4. alentin S., Schreiber S., Haupt V.J., Adasme M.F., Schroeder M. PLIP: fully automated protein–ligand interaction profiler,Nucleic Acids Res. 2015 Jul 1; 43(W1): W443–W447.
5. Krivák R, Hoksza D. P2Rank: machine learning based tool for rapid and accurate prediction of ligand binding sites from protein structure. J Chem 2018;10:1–12.
6. Guilloux V.L., Schmidtke P., Tuffery P. Fpocket: an open source platform for ligand pocket detection. BMC Bioinformatics. 2009; 10:168.
7. Mylonas, S. K., Axenopoulos, A. & Daras, P. DeepSurf: a surface-based deep learning approach for the prediction of ligand binding sites on proteins. Bioinformatics 37, 1681–1690 (2021).
8. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
9. Kwon Y, Shin WH, Ko J, Lee J. AK-Score: Accurate Protein-Ligand Binding Affinity Prediction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
