# Description

Prediction model retrained by adding data to [MF-SuP-pKa](https://www.sciencedirect.com/science/article/pii/S2211383522004622), a pKa prediction model.

Predicts acid pKa and base pKa, and ionization proceeds if they are lower or higher than the desired pH \.
If the results of acid pKa and base pKa conflict, the result is a large difference from the pH.

---
# Inputs
### Query compounds
 - Drawing : If you draw the compound in 2D and hit <b>Import drawings</b>, it will be entered as smiles.
 - Smiles : Add Smiles and name.

### Standardization
Normalize the charge of Smiles before calculating pKa.

### Molecular ionization calculated at pH
Calculate the charge of a molecule based on its pH.

---
# Outputs
## Web page
### Summary

|Columns|Description|etc|
|:-:|:-:|:-:|
|Name|이름||
|Std Acid pKa|Standardized compound's Acid pKa prediction|If lower than pH - may be charged|
|Std Base pKa|Standardized compound's Base pKa prediction|If higher than pH + may be charged|
|Std SMILES|Smiles in Standardized Compounds||
|Chg Acid pKa|Predicted Charge Predicted Acid pKa of the compound|If lower than pH - may be charged|
|Chg Base pKa|Predicted Charge Predicted Base pKa of the compound|If higher than pH + may be charged|
|Chg SMILES|Smiles of Predicted Charge Compounds||
|Charge|Predicted total charge||

#### If pKa is 0, no charge can be attached

## Download File
 - pKa.charge_smiles.smi : Smiles of Predicted Charge Compounds
 - pKa.summary.tsv : Same as Summary on Web
 - pKa.extend.tsv : pKa of all calculated charge Smiles
 - failed_compounds.tsv : The name of the molecule for which the prediction failed and the reason.
 
---
# References
1. Wu, J., Wan, Y., Wu, Z., Zhang, S., Cao, D., Hsieh, C. Y., & Hou, T. (2022). MF-SuP-pKa: multi-fidelity modeling with subgraph pooling mechanism for pKa prediction. Acta Pharmaceutica Sinica B.
