# Description

Autodock-GPU과 Vdock을 이용하여 500만개 이상의 small molecule에 대해서 docking 결과를 가져온다.

# Inputs

- `protein receptor` [5UOR.A_protein.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/input/5UOR.A_protein.pdb)

# Outputs

- [vdock_screening.dock.BINDING_E.pdbqt](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.BINDING_E.pdbqt) : Best ligand 3d file
- [vdock_screening.dock.receptor.pdb](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.receptor.pdb) : Protein receptor 3d file
- [vdock_screening.dock.report.tsv](https://docs.ad3.io/media/apps/dock_millions/examples/output/vdock_screening.dock.report.tsv) : Best ligand data

# References

1. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
2. Choi, J. & Lee, J. V-Dock: Fast Generation of Novel Drug-like Molecules Using Machine-Learning-Based Docking Score and Molecular Optimization. Int J Mol Sci 22, 11635 (2021). Journal
