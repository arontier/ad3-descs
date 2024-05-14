# Description

pKa 예측 모델인 [MF-SuP-pKa](https://www.sciencedirect.com/science/article/pii/S2211383522004622)에 데이터를 추가하여 재학습한 예측모델

acid pKa와 base pKa를 예측하며, 각각 원하는 pH에 보다 낮거나 높으면 ionization이 진행된다. \
acid pKa와 base pKa의 결과가 충돌하게 되면 pH과의 차이가 큰 결과를 따른다. 

---
# Inputs
### Query compounds
 - Drawing : 2D로 화합물을 그리고 <b>Import drawings</b>을 누르면 smiles로 입력됩니다.
 - Smiles : Smiles와 이름을 넣어주세요.

### Standardization
pKa 계산하기 전에 Smiles의 Charge를 표준화합니다.

### Molecular ionization calculated at pH
분자의 Charge를 pH에 맞춰 계산합니다.

---
# Outputs
## Web page
### Summary

|Columns|Description|etc|
|:-:|:-:|:-:|
|Name|이름||
|Std Acid pKa|Standardization된 화합물의 Acid pKa 예측값|pH보다 낮으면 - Charge가 붙을 수 있음|
|Std Base pKa|Standardization된 화합물의 Base pKa 예측값|pH보다 높으면 + Charge가 붙을 수 있음|
|Std SMILES|Standardization된 화합물의 Smiles||
|Chg Acid pKa|예측된 Charge 화합물의 Acid pKa 예측값|pH보다 낮으면 - Charge가 붙을 수 있음|
|Chg Base pKa|예측된 Charge 화합물의 Base pKa 예측값|pH보다 높으면 + Charge가 붙을 수 있음|
|Chg SMILES|예측된 Charge 화합물의 Smiles||
|Charge|예측된 총 Charge||

#### pKa가 0이면 Charge가 붙을 수 없음

## Download File
 - pKa.charge_smiles.smi : 예측된 Charge 화합물의 Smiles
 - pKa.summary.tsv : Web의 Summary와 동일
 - pKa.extend.tsv : 계산된 모든 charge Smiles의 pKa
 - failed_compounds.tsv : 예측이 실패한 분자의 이름과 이유입니다.
 
---
# References
1. Wu, J., Wan, Y., Wu, Z., Zhang, S., Cao, D., Hsieh, C. Y., & Hou, T. (2022). MF-SuP-pKa: multi-fidelity modeling with subgraph pooling mechanism for pKa prediction. Acta Pharmaceutica Sinica B.
