# Description

구조 유사성을 이용한 특허의 화합물을 검색입니다. \
Query Compound와 특허 화합물의 fingerprint를 Tanimotoy coefficient 계산하여 유사성을 측정합니다. \
Fingerprint 마다 구조의 구분 정밀도가 차이가 있습니다.

- ECFP : high
- FCFP : medium
- MACCSKey : low


\*구조의 구분 정밀도가 높다면 similarity가 낮게 측정될수 있습니다.\
\*Tanimoto coefficient가 너무 낮으면, 유사성 있는 화합물이 너무 많이 검색됩니다.

---
# Inputs
### Query compounds
 - Drawing : 2D로 화합물을 그리고 Import drawings을 누르면 SMILES로 입력됩니다.
 - SMILES : SMILES와 이름을 넣어주세요.

### Fingerprint selection
- Extended Connectivity Fingerprint(r=2, h=1024) : ECFP
- Function Class Fingerprints(r=2, h=1024) : FCFP
- MACCS Fingerprints

### Cutoff : Simiarity cutoff

#### 추천 조합
  - ECFP, 0.7
  - FCFP, 0.7
  - MACCS, 0.8

---
# Outputs
## Web page
### Target
입력한 분자의 SMILES와 2D 이미지입니다.

### Search
입력한 분자와 유사한 patent의 정보입니다.

|Name|Description|etc|
|:-:|:-:|:-:|
|Query|입력된 분자의 SMILES와 2D 이미지||
|Compound|Query와 유사한 화합물의 SMILES와 2D 이미지||
|Similarity|계산된 Tanimoto coefficient||
|AD3 Patent id|AD3에 저장되어 있는 Patent 정보||
|Patent Country|특허 국가 코드||
|Patent id|특허 번호|Google patent로 연동||
|Patent Title|특허 제목||
|Patent year|특허 발행년도||

## Download file
- PS.summary.tsv : Summary 파일입니다.
- PS.exact.tsv : Similarity가 1인 화합물들입니다.

---
# References
