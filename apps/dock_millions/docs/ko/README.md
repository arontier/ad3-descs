# Description

분자 모델링 시뮬레이션 소프트웨어인 Autodock-GPU과 머신러닝을 이용한 docking score 모델인 Vdock을 이용하여 500만개에서 5000만개의 small molecule( MW :150~500 )을 원하는 단백질 대해서 docking 결과를 가져옵니다.

# Inputs

- `protein receptor` [5UOR.A_protein.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/input/5UOR.A_protein.pdb)
- Number of iteration : Docking 및 머신러닝의 재학습의 반복 횟수
- Initial screen data : 첫번째 Docking 데이터이며, similarity를 이용한 clustering한 데이터 베이스
  - NR10 : similarity < 10, 약 6,000
  - NR15 : similarity < 15, 약 35,000
  - NR20 : similarity < 20, 약 140,000
- Screen data
  - Mcule purchasable : Mcule사의 instock 화합물, 약 5M
  - Enamine lead-like : Enamine사의 Real Diversity set, 약 38.2M
- Docking number of data

# Outputs

- [vdock_screening.dock.BINDING_E.pdbqt](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.BINDING_E.pdbqt) : Best ligand 3d file
- [vdock_screening.dock.receptor.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.receptor.pdb) : Protein receptor 3d file
- [vdock_screening.dock.report.tsv](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.report.tsv) : Best ligand data

# References

1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal
3. [Mcule database](https://mcule.com/database/)
4. [Enamine database](https://enamine.net/compound-collections/real-compounds/real-database-subsets)
