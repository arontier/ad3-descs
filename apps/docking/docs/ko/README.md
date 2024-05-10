<!-- @format -->

# Description

Autodock-GPU를 이용하여 단백질과 분자들 사이의 결합세기를 측정합니다. \
Scoring 방법으로 Autodock4와 AK-Score2를 이용합니다.

# Inputs
 ### Target : 단백질 구조 
 - Public : 단백질 이름을 검색할 수 있습니다.
   - Alphafold model 또는 PDB 구조 선택합니다.
 - private : TARGETS 메뉴에서 추가된 단백질을 선택합니다.

 ### Binding Site : 분자가 결합할 위치, 선택된 Residue들의 중심
 - Site : Site 앱에서 예측, Docking 될 부분 선택합니다.
 - Residue : Site를 선택하지 않으면, 직접 Residue number를 입력 가능합니다.
   
### Ligand : 분자
 - Ligand : sdf 또는 pdb 또는 mol2 파일을 넣을 수 있습니다.

   pdb는 CONECT를 포함되어야 정확한 분자 결합이 표현됩니다.

# Outputs
## Web page
### Target
단백질 구조의 길이와 3D 구조를 살펴볼 수 있습니다.
### Result
분자가 단백질과 결합된 구조와 3개의 binding energy (AK-Score2 Energy, Autodock Energy, Autodock Cluster Energy)를 보여주고 있습니다.

## Download File
 - Dock.report.tsv : 결과 테이블로 UID, AK_E, BINDING_E, CLUSTER_E와 각각의 RANK, CANON_SMILES를 포함하고 있습니다.
 - Dock.AK_E : 각 분자에 대한 AK-Score2에 대한 구조로 pdb파일과 sdf파일이 있습니다.
 - Dock.BINDING_E : 각 분자에 대한 autodock energy에 대한 구조로 pdb파일과 sdf파일이 있습니다.
 - Dock.CLUSTER_E :각 분자에 대한 autodock cluster energy에 대한 구조로 pdb파일과 sdf파일이 있습니다.
 - Dock.receptor.pdb : 단백질 구조 파일입니다.
 - failed_ligand.tsv : Docking이 실패한 분자에 대한 이름과 이유입니다.
# References
1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. AK-Score: Accurate Protein-Ligand Binding Affinity Prediction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
