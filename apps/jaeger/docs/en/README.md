# Description

JTGEN is a deep generation for small molecule generation. JTGEN is based on the Junction-Tree Variational Auto-Encoder (JT-VAE) method to generate chemically valid molecules.

When creating new molecules, you define a search strategy to efficiently explore the potential space. JTGEN combines potential space exploration with an active predictive model to generate and optimize new molecules.
1. JTGEN is trained on existing molecules with assay results or docking results.
2. During training, it learns how to map the latent space (high dimensional) and decode back to molecules in the latent space.
3. Explore the potential space to generate new molecules.

---
## Ouput description
# Inputs
### TRAINGING DATA
 - TSV or CSV : Docking summary file or pIC50
   - The head columns must have SMAILES (or CANON_SMILES), AK_E (or BINDING_E or SCORE).
   - If AK_E, BIDNDING_E, and SCORE are present, they are prioritized in the order AK_E, BINDING_E, and SCORE.
   - The higher the SCORE, the better, and the lower the AK_E and BINDING_E, the better.
 - The more data have, the longer the training time

**N.B.:** If **AK_E**, **SCORE**, and **BINDING_E** are present in the tsv file at the same time, only one will be trained for prediction and it will be predicted in the order of AK_E, BINDING_E, and SCORE. \
**N.B.:** The model filters out all molecules with more than 50 atoms.  \
**N.B.:** smiles should not have "."

### SELECT SMILES 
 - Use it as a starting point for creating molecules.
 - The more you select, the more compounds will be generated (we recommend selecting at least 10).

---
# Outputs
## Web page
### Summary
Score, MW, QED, logP of generated compounds
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
 - failed_generate.tsv : If you put generation smiles in, why didn't it generate with smiles?

---
# References
1. JAEGER :Godinez, W. J. & Ma, E. J. Novartis/JAEGER: Public. Zenodo, doi:https://doi.org/10.5281/zenodo.5794429 (2021).

2. Junction Tree Variational Autoencoder for Molecular Graph Generation\
*Wengong Jin, Regina Barzilay, Tommi S. Jaakkola: Junction Tree Variational Autoencoder for Molecular Graph Generation. ICML 2018: 2328-2337 https://arxiv.org/abs/1802.04364
