# Description

구조 유사성을 이용한 특허의 화합물을 검색 \
Query Compound와 특허 화합물의 fingerprint 구하고 Tanimotoy coefficient를 계산하여 유사성을 측정 \
Fingerprint 마다 구조의 구분 정밀도가 차이가 있다.

- ECFP : high
- FCFP : medium
- MACCSKey : low

\*구조의 구분 정밀도가 높다면 similarity가 낮게 측정될수 있습니다.\
\*Tanimoto coefficient가 너무 낮으면, 유사성 있는 화합물이 너무 많이 검색됨.

# Inputs

- `Query Compounds` [example.smi](https://openapi.ad3.io/media/apps/chemical_patents/examples/input/example.smi)
- Model selection
  - Extended Connectivity Fingerprint(r=2, h=1024) : ECFP
  - Function Class Fingerprints(r=2, h=1024) : FCFP
  - MACCS Fingerprints
- Tanimoto coefficient : Simiarity cutoff

- 추천 조합
  - ECFP, 0.7
  - FCFP, 0.7
  - MACCS, 0.8

# Outputs

# References
