# Description
### Molfinder
Molfinder puts random compounds into a <b>bank</b> and the lowest-scoring compounds into a <b>seed</b> and performs crossover and mutation between the seed and bank to find new compounds.
<img src="https://github.com/arontier/ad3-descs/assets/98073046/d504a64b-e38a-4376-ba42-3deb2594de52" width="70%" height="70%">


---
# Inputs
### Choose weighted models
 - TSV : Docking summary file or pIC50
   - The head columns must have SMAILES (or CANON_SMILES), AK_E (or BINDING_E or SCORE).
   - If AK_E, BIDNDING_E, and SCORE are present, they are prioritized in the order AK_E, BINDING_E, and SCORE.
   - The higher the SCORE, the better, and the lower the AK_E and BINDING_E, the better.

### Choose weighted method
 - QED : quantitative estimate of drug-likeness
 - J-Score : logP - SAscore -Ring penalty - Size penalty
 - Drug score : Drug score made with DMPNN model

#### weight :  The higher the number, the higher the percentage of that Score.

### Penalties : Must meet those conditions.
 - Lipinski : Lipinski's rule of five, MW <= 550, HBD <= 5, HBA <= 10, logP <= 5 
 - Spiro : Spiro Atoms <= 1
 - Bridgehead : Bridgehead = 0
 - Ring : Ring size 5 or 6
 - Logp : lopg <= 6.5
 - SA : SAscore <= 3.5
 - Nring : number or Ring <= 4
 - Hetero : Hetero Atom (heavy atom not C) 수 <= 8
 - PAINS : PAINS filter = 0
 - Brenk : Brenk filter = 0
 - NIH : NIH fitler = 0

---
# Outputs
## Web page
### Summary
id, Score, MW, QED, logP, Smiles of the generated compounds.

### Results
Histogram for each Scores.

## Download File
 - MF-reuslt.tsv : Summary file
 - MF-result.smi : Smiles file


---
# References
1. Kwon, Y.; Lee, J. MolFinder: An Evolutionary Algorithm for the Global Optimization of Molecular Properties and the Extensive Exploration of Chemical Space Using SMILES. J. Cheminform. 2021, 13 (1), 24.
2. G. R. Bickerton, G. V. Paolini, J. Besnard, S. Muresan and A. L. Hopkins, Quantifying the chemical beauty of drugs Nat. Chem., 2012, 4, 90–98.
