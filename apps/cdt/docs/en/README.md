# Description

1. Find the Maximum Common Substructure (MCS) between two molecules.
2. Calculate the <b>Similarity</b> ($\frac{atoms in MCS}{atoms in molecule}$) of the number of atoms occupied by MCS in the molecule.
3. If Similarity is greater than to Cutoff, connect in the direction of the greater value.

---
# Inputs
### Query compounds
- Drawing : If you draw the compound in 2D and hit Import drawings, it will be entered as smiles.
- Smiles : Add Smiles and name.

### SMILES of root node
Insert the SMILES that will be the starting point(Root) for the tree. \
ex) 'CCCCC'

### Similarity(MCS) cutoff
If the value of <b>Similarity</b> ($\frac{atoms in MCS}{atoms in molecule}$) is greater than the Cutoff, they are connected.

---
# Outputs
## Web page
### Relationships between compounds
Calculate the similarity between the molecules and draw a clustermap. \
The Similarity value is the average of the similarity between the two molecules.

### Diversity tree
- This is the tree from top to bottom.
- The MCS of the compounds are colored in red.
- The numbers in the connections are Similarity. 

## Download file
- CDT.CDT_LR.jpg : The left side is the rooted tree.
- CDT.CDT_TB.jpg : The tree at the top is the root.
- CDT.cluster_map.png : Cluster map.

---
# References
1. Péter Englert and Péter Kovács. Efficient Heuristics for Maximum Common Substructure Search . Journal of Chemical Information and Modeling, 2015, 55:941-955.
2. John W. Raymond and Peter Willett. Maximum common subgraph isomorphism algorithms for the matching of chemical structures . Journal of Computer-Aided Molecular Design, 2002, 16:521-533.
3. Takeshi Kawabata. Build-up algorithm for atomic correspondence between chemical structures . Journal of Chemical Information and Modeling, 2011, 51:1775-1787.
