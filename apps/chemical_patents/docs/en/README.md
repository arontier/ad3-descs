# Description

Search for compounds in patents using structural similarity \
Obtain fingerprints of the query compound and the patented compound and calculate the Tanimotoy coefficient to measure the similarity \
Different fingerprints have different structure identification precision.

- ECFP : high
- FCFP : medium
- MACCSKey : low

\*If the structure identification precision is high, the similarity may be low.\
\*If the Tanimoto coefficient is too low, too many similar compounds are searched.

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
