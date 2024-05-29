# Description
JT-VAE Generative Modeling (JAEGER) is a deep generative approach for small-molecule design. JAEGER is based on the Junction-Tree Variational Auto-Encoder (JT-VAE) method [1], which ensures chemical validity for the generated molecules.

JAEGER is trained on existing molecules associated with activity values measured in a given assay. During training, JAEGER learns how to map each molecule onto a (high-dimensional) coordinate space, often referred to as the latent space. JAEGER also learns how to decode a coordinate position in the latent space back to a molecule.

To generate new molecules, JAEGER defines numerical search strategies to efficiently and effectively explore that latent space. JAEGER couples the exploration of that latent space together with activity predictive models to discover and optimize novel active molecules.

## Ouput description
|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|
|SCORE|Prediction SCORE||lower is best|
|QED|Quantifying the chemical beauty of drugs||0~1(Best)|
|MW|Molecule Weight|g/mol||
|LogP|octanol/water parition coefficient|||

# Inputs
```
TRAINGING DATA :  tsv file must have CANON_SMILES and have SCORE (higher is better) or BINDING_E (Docking output file) or AK_E (AKscore2 output file).
SELECT SMILES : Starting point for molecule generation. The more select, the more compounds will be generated. (Recommend selecting at least 10)
```




# Description

JTGEN is a deep generation for small molecule generation. JTGEN is based on the Junction-Tree Variational Auto-Encoder (JT-VAE) method to generate chemically valid molecules.

When creating new molecules, you define a search strategy to efficiently explore the potential space. JTGEN combines potential space exploration with an active predictive model to generate and optimize new molecules.
1. JTGEN is trained on existing molecules with assay results or docking results.
2. During training, it learns how to map the latent space (high dimensional) and decode back to molecules in the latent space.
3. Explore the potential space to generate new molecules.

Translated with www.DeepL.com/Translator (free version)


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
