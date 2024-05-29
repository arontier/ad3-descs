# Description

JTGEN은 소분자 생성을 위한 deep generation 입니다. JTGEN는 Junction-Tree Variational Auto-Encoder (JT-VAE) method을 기반으로 화학적 유효성을 유지한며 분자를 생성합니다.

새로운 분자를 만들 떄 효율적으로 잠재 공간을 탐색하기 위해 검색 전략을 정의합니다. JTGEN는 잠재공간 탐색과 active 예측모델을 결합하여 새로운 분자를 생성하고 최적화 합니다.
1. JTGEN는 assay 결과나 Docking 결과를 가지고 기존 분자에 대해서 훈련합니다.
2. 훈련 중에 잠재공간(고차원)의 매핑하는 방법을 배우고 잠재공간에서 다시 분자로 해독하는 방법을 배웁니다.
3. 잠재공간을 탐색하여 새로운 분자를 생성합니다.


---
## Ouput description
# Inputs
### TRAINGING DATA
 - TSV or CSV : Docking summary file or pIC50
   - head columns에 SMAILES (or CANON_SMILES), AK_E(or BINDING_E or SCORE)가 있어야 합니다.
   - AK_E, BIDNDING_E, SCORE가 같이 있다면 AK_E, BINDING_E, SCORE 순으로 우선 순위가 있습니다.
   - SCORE는 높을수록 좋음, AK_E와 BINDING_E가 낮을수록 좋습니다.
 - Data가 많을 수록 학습시간이 오래 걸립니다. (기본 10시간)


**N.B.:** tsv파일에 **AK_E**, **BINDING_E**, **SCORE**가 동시에 있다면 한가지만 예측에 이용되며, AK_E, BINDING_E, SCORE 순으로 예측을 합니다. \
**N.B.:** 분자의 atom 갯수가 50개가 넘어가면 filter에 걸려 들어가지 않음\
**N.B.:** smiles에 "." 이 들어가면 안됨.
### SELECT SMILES 
 - 분자 생성의 시작점으로 사용합니다.
 - 많이 선택할수록 많은 화합물이 생성됩니다. (최소 10개를 선택하길 바랍니다.)

---
# Outputs
## Web page
### Summary

생성된 화합물의 Score, MW, QED, logP
|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|
|SCORE|SCORE 예측||lower is best|
|MW|Molecule Weight|g/mol||
|QED|Quantifying the chemical beauty of drugs||0~1(Best)|
|LogP|octanol/water parition coefficient|||

### Histogram
생성된 화합물의 Score, MW, QED, logP의 histogram

## Download File
 - JG-result.tsv : Result summary file
 - JG-result.smi : Result smiles file
 - failed_generate.tsv : 생성에 사용된 Smiles 중에 실패한 Smiles들과 그 이유입니다.

---
# References
1. JAEGER :Godinez, W. J. & Ma, E. J. Novartis/JAEGER: Public. Zenodo, doi:https://doi.org/10.5281/zenodo.5794429 (2021).

2. Junction Tree Variational Autoencoder for Molecular Graph Generation\
*Wengong Jin, Regina Barzilay, Tommi S. Jaakkola: Junction Tree Variational Autoencoder for Molecular Graph Generation. ICML 2018: 2328-2337 https://arxiv.org/abs/1802.04364
