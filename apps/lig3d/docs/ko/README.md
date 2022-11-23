# Description 

Lig3D는 화합물의 1차원 혹은 2차원 정보를 입력받아 Docking에 필요한 3차원 구조를 생성하는 앱입니다. 화합물 생성은 RDKit의 ETKDGv3방법을 이용합니다. [1][2]

# Input

Lig3D의 입력은 화합물의 1차원 혹은 2차원 정보를 담고 있는 4가지 형식의 파일(smi, pdb, mol2, sdf)형식의 파일을 이용할 수 있습니다.

* 예시) [AD3XX00000152.MAPK14.activities.smi](AD3XX00000152.MAPK14.activities.smi)

# Outputs

결과는 입력된 화합물의 3차원 구조를 저장한 3가지 형식의 파일(pdb,sdf,mol2)과 3차원 구조 생성 결과를 정리한 1개의 TSV파일을 담고 있습니다. 3차원 결과 파일은 모두 동일한 정보를 담고 있습니다.

# References
1. Wang, S., Witek, J., Landrum, G. A. & Riniker, S. Improving Conformer Generation for Small Rings and Macrocycles Based on Distance Geometry and Experimental Torsional-Angle Preferences. J Chem Inf Model 60, 2044–2058 (2020).
2. https://www.rdkit.org/docs/source/rdkit.Chem.rdDistGeom.html
