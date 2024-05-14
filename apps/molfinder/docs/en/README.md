# Description
### Molfinder
Molfinder-Scaffold fetches fragments from the database based on the input scaffold and combines them with the scaffold. \
 The existing Molfinder operation only works on fragments and adds a selection that randomizes the fragments to find new compounds.
![image](https://github.com/arontier/ad3-descs/assets/98073046/d504a64b-e38a-4376-ba42-3deb2594de52)

### Database
 - GDB-11(179,173,826) : enumerates small organic molecules up to 11 atoms of C, N, O and F following simple chemical stability and synthetic feasibility rules.
 - Library(367,063) : Fragment database in Mcuel and Enamine
 - Enamine(2,993) : Essential Fragment Library,High Fidelity Fragment Library,DSI-poised Library in Enamine. Deduplicated
 - Mini(2,025) : Mcule and Enamine's mini fragment database, compounds with 7 or fewer heavy atoms.

#### Mini and Enamine have no effect on the fragment size option.
#### For databases other than GDB-11, if the number of *'s is 1, it will fragment as much as possible and take the best.

---
# Inputs
### Query compound
 - Drawings : Simply draw a compound, type R where you want to attach the fragment, and hit <b>Import drawings</b>.
 - Samiles : Simply put in the Scaffold you want and put an (*) where you want to attach the fragment.

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
### Target
Score, MW, QED, logP, Smiles of the scaffold compound
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
3. Fink, T.; Reymond, J.-L. Virtual exploration of the chemical universe up to 11 atoms of C, N, O, F: assembly of 26.4 million structures (110.9 million stereoisomers) and analysis for new ring systems, stereochemistry, physico-chemical properties, compound classes and drug discovery. J. Chem. Inf. Model. 2007, 47, 342-353.
4. [Mcule database](https://mcule.com/database/)
5. [Enamine database](https://enamine.net/compound-libraries/fragment-libraries)
