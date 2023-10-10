# Description

### Reverse docking
하나의 ligand를 여러 단백질에 Docking하여 ligand 결합 에너지를 측정하는 방법이다. \
ligand에 대한 잠재적 단백질을 식별할 수 도 있고, 약물의 독성에 대해서 알아보는데 사용되기도 합니다.

### Fittest
 여러 ligand들에 대한 공통 또는 동시에 Target 되는 단백질을 찾는 방법이다. \
 ligand들 마다 결합된 단백질의 score를 Z-score로 표준화하고 Z-score의 합산을 통해 ligand들에 가장 결합 가능성이 높은 단백질을 찾는다. 

### method
* Docking : Autodoc GPU
* Scoreing : AKscore2 

# Inputs
sdf or pdb
# Outputs

# References
