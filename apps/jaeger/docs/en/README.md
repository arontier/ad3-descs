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
tsv file :  tsv file must have CANON_SMILES and have SCORE (higher is better) or BINDING_E (Docking output file) or AK_E (AKscore2 output file).
generation smiles : The smiles in the tsv file are the starting point for molecule generation.
```
**N.B.:** The model filters out all molecules with more than 50 atoms. 

**N.B.:** smiles should not have "."
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
