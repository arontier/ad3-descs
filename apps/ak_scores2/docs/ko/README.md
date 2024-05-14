# Description

단백질과 화합물 결합구조를 입력받아 AK-Score2 energy를 계산합니다.

---
# Inputs
 ### Target : 단백질 구조 
 - Public : 단백질 이름을 검색할 수 있습니다.
   - Alphafold model 또는 PDB 구조 선택합니다.
 - private : TARGETS 메뉴에서 추가된 단백질을 선택합니다.

### Ligand : 분자 (pdb)
단백질과 결합하고 있는 분자의 3D구조 파일을 넣습니다.

   pdb는 CONECT를 포함되어야 정확한 분자 결합이 표현됩니다.

---
# Outputs
## Web page
### Target
단백질 구조의 길이와 3D 구조를 살펴볼 수 있습니다.
### Result
분자가 단백질과 결합된 구조와 AK-Score2 Energy를 보여주고 있습니다.

## Download File
 - AKscore.report.tsv : 결과 테이블로 UID, akscore2_nondock, akscore2_dock, akscore2_nondock_mul_dock, autodock_score, AK_E, AK_E_RANK, CANON_SMILES, INCHIKEY을 포함합니다.
 - AKscore.AK_E : 각 분자에 대한 AK-Score2에 대한 구조로 pdb파일과 sdf파일이 있습니다.
 - AKscore.receptor.pdb : 단백질 구조 파일입니다.
 - failed_ligand.tsv : AKscore2 계산이 실패한 분자에 대한 이름과 이유입니다.


---
# References
1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. AK-Score: Accurate Protein-Ligand Binding Affinity Prediction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
