# Description

 분자 도킹 예측 프로그램인 Autodock-GPU과 머신러닝을 이용한 docking score 모델인 Vdock을 이용하여 500만개에서 5000만개의 small molecule( MW :150~500 )을 단백질 대해서 docking 결과를 가져옵니다.
 
---------------------
# Inputs
 ### Target : 단백질 구조 
 - Public : 단백질 이름을 검색할 수 있습니다.
   - Alphafold model 또는 PDB 구조 선택합니다.
 - private : TARGETS 메뉴에서 추가된 단백질을 선택합니다.

 ### Binding Site : 분자가 결합할 위치, 선택된 Residue들의 중심
 - Site : Site 앱에서 예측, Docking 될 부분 선택합니다.
 - Residue : Site를 선택하지 않으면, 직접 Residue number를 입력 가능합니다.

 ### Screening option : 
- Number of iteration : Docking 및 머신러닝 학습의 반복 횟수
- Initial screen data : 첫번째 Docking 데이터이며, similarity를 이용한 clustering한 데이터 베이스
  - NR10 : similarity < 10, 약 6,000
  - NR15 : similarity < 15, 약 35,000
  - NR20 : similarity < 20, 약 140,000
- Screen data
  - Mcule purchasable : Mcule사의 instock 화합물, 약 5M
  - Enamine lead-like : Enamine사의 Real Diversity set, 약 38.2M
- Docking number of data
  - iteration 당 Docking 되는 ligand 수 (작을 수록 시간 소요가 적고 많을 수록 정확도가 높아짐) 
- Lipinsk's rule of five : 스크리닝하는 분자의 조건을 겁니다.
  - Molecule Weight <= 500
  - Hydrogen bond donor <= 5
  - Hydroget bond acceptor <= 10
  - LogP <= 5.0 

 ### V-Dock option : 
 - Method : 머신러닝 종류 선택입니다.
 - Feature : 머신러닝에 사용될 분자의 feature 종류입니다.
  
---------------------
# Outputs
## Web page
### Target
단백질 구조의 길이와 3D 구조를 살펴볼 수 있습니다.
### Seed docking
 - Initial screen data에 대한 binding energy distribution
 - 분자와 interaction하는 Residue들의 빈도 수와 interaction type 
### Hit Candidates 
AK-Score2 Energy을 기준으로 상위의 분자들에 대한 단백질과 결합된 구조와 3개의 binding energy (AK-Score2 Energy, Autodock Energy, Autodock Cluster Energy)를 보여주고 있습니다.

## Download File
 - vdock_screening.dock.report.tsv : 결과 테이블로 UID, AK_E, BINDING_E, CLUSTER_E와 각각의 RANK, CANON_SMILES를 포함하고 있습니다.
 - vdock_screening.dock.AK_E : 각 분자에 대한 AK-Score2에 대한 구조로 pdb파일과 sdf파일이 있습니다.
 - vdock_screening.dock.receptor.pdb : 단백질 구조 파일입니다.
 - DOCK.report.pdf : 정리된 PDF파일입니다.
 
---------------------
# References

1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal
3. [Mcule database](https://mcule.com/database/)
4. [Enamine database](https://enamine.net/compound-collections/real-compounds/real-database-subsets)
