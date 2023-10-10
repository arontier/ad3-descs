# Description
사람의 모든 단백질을 이용하여 여러 ligand들의 결합의 가능성이 높은 단백질을 찾아내는 방법
### Reverse docking
하나의 ligand를 여러 단백질에 Docking하여 ligand와 결합 가능성이 높은 단백질을 찾아내는 방법

### Fittest
 ligand들 마다 결합된 단백질의 score를 Z-score로 표준화하고 Z-score의 합산을 통해 ligand들에 가장 결합 가능성이 높은 단백질을 찾는다. 

### method
* Docking : Autodoc GPU
* Scoreing : AKscore2 

# Inputs
sdf or pdb
# Outputs

# References
