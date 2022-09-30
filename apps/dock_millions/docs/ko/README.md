##도움말
분자 모델링 시뮬레이션과 머신러닝을 이용하여 단백질과 500만개에서 5000만개의 분자 사이의 결합 세기가 강한 분자를 찾습니다.

# Description

분자 모델링 시뮬레이션 소프트웨어인 Autodock-GPU과 머신러닝을 이용한 docking score 모델인 Vdock을 이용하여 500만개에서 5000만개의 small molecule( MW :150~500 )을 원하는 단백질 대해서 docking 결과를 가져옵니다.

# Inputs

- `protein receptor` [5UOR.A_protein.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/input/5UOR.A_protein.pdb)

# Outputs

- [vdock_screening.dock.BINDING_E.pdbqt](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.BINDING_E.pdbqt) : Best ligand 3d file
- [vdock_screening.dock.receptor.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.receptor.pdb) : Protein receptor 3d file
- [vdock_screening.dock.report.tsv](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.report.tsv) : Best ligand data

# References

1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal
