# Description

Search for compounds in patents using structural similarity \
Obtain fingerprints of the query compound and the patented compound and calculate the Tanimotoy coefficient to measure the similarity \
Different fingerprints have different structure identification precision.

- ECFP : high
- FCFP : medium
- MACCSKey : low

\*If the structure identification precision is high, the similarity may be low.\
\*If the Tanimoto coefficient is too low, too many similar compounds are searched.

---
# Inputs
### Query compounds
 - Drawing : If you draw the compound in 2D and hit Import drawings, it will be entered as smiles.
 - Smiles : Add Smiles and name.

### Fingerprint selection
- Extended Connectivity Fingerprint(r=2, h=1024) : ECFP
- Function Class Fingerprints(r=2, h=1024) : FCFP
- MACCS Fingerprints

### Cutoff : Simiarity cutoff

#### Suggested combinations
  - ECFP, 0.7
  - FCFP, 0.7
  - MACCS, 0.8

---
# Outputs
## Web page
### Target
The SMILES and 2D image of the molecule you entered.

### Search
Information from the patent that is similar to the molecule you entered.

|Name|Description|etc|
|:-:|:-:|:-:|
|Query|SMILES and 2D images of the input molecules||
|Compound|SMILES and 2D images of compounds similar to the query.||
|Similarity|Calculated Tanimoto coefficient||
|AD3 Patent id|Patent information stored in AD3||
|Patent Country|Patent country code||
|Patent id|Patent number|Integration with Google patents||
|Patent Title|Patent name||
|Patent year|patent filing year||

## Download file
- PS.summary.tsv : Summary file.
- PS.exact.tsv : Compounds with a similarity of 1.

---
# References
