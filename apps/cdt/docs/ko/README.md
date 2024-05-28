# Description

1. 두 분자 사이의 Maximum Common Substructure (MCS)을 찾습니다.
2. 분자에서 MCS가 차지하는 atom 수가 <b>Similarity</b> ($\frac{MCS의\ atoms}{분자의\ Atoms}$)를 계산합니다.
3. Similarity가 Cutoff 이상이라면 값이 큰 방향으로 연결합니다.

---
# Inputs
### Query compounds
- Drawing : 2D로 화합물을 그리고 Import drawings을 누르면 smiles로 입력됩니다.
- Smiles : Smiles와 이름을 넣어주세요.

### SMILES of root node
Tree의 시작점이 될 SMILES를 넣습니다.
예) 'CCCCC'

### Similarity(MCS) cutoff
<b>Similarity</b> ($\frac{MCS의\ atoms}{분자의\ Atoms}$)의 값이 Cutoff 보다 크면 연결됩니다.

---
# Outputs
## Web page
### Relationships between compounds
분자들 사이의 Similarity를 계산하고 Clustermap을 그립니다. \
Similarity 값은 두 분자 사이의 Similarity의 평균입니다.

### Diversity tree
- 위에서부터 아래로 내려가는 Tree입니다.
- 화합물에 MCS가 빨간색으로 그려져 있습니다.
- 연결부분의 숫자는 Similarity입니다. 

## Download file
- CDT.CDT_LR.jpg : 왼쪽이 뿌리가 되는 Tree입니다.
- CDT.CDT_TB.jpg : 위가 뿌리가 되는 Tree입니다.
- CDT.cluster_map.png : Cluster map입니다.

---
# References
1. Péter Englert and Péter Kovács. Efficient Heuristics for Maximum Common Substructure Search . Journal of Chemical Information and Modeling, 2015, 55:941-955.
2. John W. Raymond and Peter Willett. Maximum common subgraph isomorphism algorithms for the matching of chemical structures . Journal of Computer-Aided Molecular Design, 2002, 16:521-533.
3. Takeshi Kawabata. Build-up algorithm for atomic correspondence between chemical structures . Journal of Chemical Information and Modeling, 2011, 51:1775-1787.
