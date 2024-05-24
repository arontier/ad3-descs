
# Description 

Lig3D is an app that takes one or two dimensional information of a compound and generates a three-dimensional structure for docking. \
The Compound generation utilizes RDKit's ETKDGv3 method. [1][2]


---
# Input
### Select Format
 - SMILES : Type SMILES directly or insert a <b>.smi, .smi.gz</b> file. 
 - Well-known format : Insert a <b>.pdb,.mol2,.sdf</b> file in a format that supports two or three dimensions.

### Query Compounds : 포멧이 SMILES인 경우
 - File : Insert a file with a file format of <b>.smi, .smi.gz</b>. 
 - Drawing : If you draw the compound in 2D and hit Import drawings, it will be entered as smiles.
 - Smiles : Add Smiles and name.

### Select File : 포멧이 Well-known formats인 경우
Insert a file with a file format of <b>.pdb, .mol2, .sdf</b>. 

---
# Outputs
## Web page
### Ligands
Shows the 3D structure of the compound.

|Name|Description|etc|
|:-:|:-:|:-:|
|Name|Compounds name|If no name is provided, it will be Ligand_[number].|
|Isomer Id|ID of the created isomer|Generate all isomers that can be generated.|
|InChiKey|A simplified version of the International Chemical Identifier(InChi).||
|Energy|The lower the energy in ETKDGv3, the more stable the structure.||
|Canonical SMILES|Canonical SMILES||
|Isomer SMILES|SMILES in an Isomer structure.||

## Download file
 - GNSS.conformers.tsv : Summary file
 - GNSS.conformers.pdb : Compounds 3D structure.
 - GNSS.conformers.sdf : Compounds 3D structure.
 - GNSS.conformers.mol2 : Compounds 3D structure.

---
# References
1. Wang, S., Witek, J., Landrum, G. A. & Riniker, S. Improving Conformer Generation for Small Rings and Macrocycles Based on Distance Geometry and Experimental Torsional-Angle Preferences. J Chem Inf Model 60, 2044–2058 (2020).
2. https://www.rdkit.org/docs/source/rdkit.Chem.rdDistGeom.html
