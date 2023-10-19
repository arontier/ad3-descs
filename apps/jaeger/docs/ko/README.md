# Description

JT-VAE Generative Modeling (JAEGER)는 소분자 생성을 위한 deep generation 입니다. JAEGER는 Junction-Tree Variational Auto-Encoder (JT-VAE) method을 기반으로 화학적 유효성을 유지한며 분자를 생성합니다.

JAEGER는 assay 결과나 Docking 결과를 가지고 기존 분자에 대해서 훈련합니다. 훈련 중에 잠재공간(고차원)의 매핑하는 방법을 배우고 잠재공간에서 다시 분자로 해독하는 방법을 배웁니다.

새로운 분자를 만들 떄 효율적으로 잠재 공간을 탐색하기 위해 검색 전략을 정의합니다. JAEGER는 잠재공간 탐색과 active 예측모델을 결합하여 새로운 분자를 생성하고 최적화 합니다.

## Ouput description
|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|
|SCORE|SCORE 예측||lower is best|
|QED|Quantifying the chemical beauty of drugs||0~1(Best)|
|MW|Molecule Weight|g/mol||
|LogP|octanol/water parition coefficient|||

# Inputs
```
tsv file : CANON_SMILES를 반드시 가지고 SCORE (higher is better) 또는 BINDING_E (Docking output file) 또는 AK_E (AKscore2 output file)을 가지고 있어야 합니다.
generation smiles : tsv파일 안에 존재하는 smiles로서 분자 생성의 시작점이 됨.
```
**N.B.:** 분자의 atom 갯수가 50개가 넘어가면 filter에 걸려 들어가지 않음

**N.B.:** smiles에 "." 이 들어가면 안됨.
# Outputs
```
JG-result.tsv : Result summary file
JG-result.smi : Result smiles file
failed_generate.tsv : If you put generation smiles in, why didn't it generate with smiles?
```
# References
JAEGER :Godinez, W. J. & Ma, E. J. Novartis/JAEGER: Public. Zenodo, doi:https://doi.org/10.5281/zenodo.5794429 (2021).

Junction Tree Variational Autoencoder for Molecular Graph Generation\
*Wengong Jin, Regina Barzilay, Tommi S. Jaakkola: Junction Tree Variational Autoencoder for Molecular Graph Generation. ICML 2018: 2328-2337 https://arxiv.org/abs/1802.04364
