# Description 

Lig3D는 화합물의 1차원 혹은 2차원 정보를 입력받아 Docking에 필요한 3차원 구조를 생성하는 앱입니다. \
화합물 생성은 RDKit의 ETKDGv3방법을 이용합니다. [1][2]

---
# Input
### Select Format
 - SMILES : SMILES를 직접 입력하거나 <b>.smi, .smi.gz</b> 파일을 넣습니다. 
 - Well-known format : 2차원 또는 3차원을 지원하는 포멧인 <b>.pdb,.mol2,.sdf</b> 파일을 넣습니다.

### Query Compounds : 포멧이 SMILES인 경우
 - File : 파일 포멧이 <b>.smi, .smi.gz</b>인 파일을 넣습니다. 
 - Drawing : 2D로 화합물을 그리고 Import drawings을 누르면 smiles로 입력됩니다.
 - Smiles : Smiles와 이름을 넣어주세요.

### Select File : 포멧이 Well-known formats인 경우
파일 포멧이 <b>.pdb,.mol2,.sdf</b>인 파일을 넣으면 됩니다.

---
# Outputs
## Web page
### Ligands
화합물의 3D 구조를 보여줍니다.

|Name|Description|etc|
|:-:|:-:|:-:|
|Name|화합물의 이름|이름을 안넣어줬다면 Ligand_number가 됩니다.|
|Isomer Id|생성된 구조의 Isomer ID||
|InChiKey|국제화학식별자(InChi)의 간략화된 버전입니다.||
|Energy|ETKDGv3의 에너지로 낮을 수록 안정된 구조입니다.||
|Canonical SMILES|SMILES의 표준상태입니다.||
|Isomer SMILES|Isomer 구조의 SMILES입니다.||

## Download file

결과는 입력된 화합물의 3차원 구조를 저장한 3가지 형식의 파일(pdb,sdf,mol2)과 3차원 구조 생성 결과를 정리한 1개의 TSV파일을 담고 있습니다. 3차원 결과 파일은 모두 동일한 정보를 담고 있습니다.

 - GNSS.conformers.tsv : Summary 파일입니다.
 - GNSS.conformers.pdb : 화합물들의 3D 구조입니다.
 - GNSS.conformers.sdf : 화합물들의 3D 구조입니다.
 - GNSS.conformers.mol2 : 화합물들의 3D 구조입니다.

---
# References
1. Wang, S., Witek, J., Landrum, G. A. & Riniker, S. Improving Conformer Generation for Small Rings and Macrocycles Based on Distance Geometry and Experimental Torsional-Angle Preferences. J Chem Inf Model 60, 2044–2058 (2020).
2. https://www.rdkit.org/docs/source/rdkit.Chem.rdDistGeom.html
