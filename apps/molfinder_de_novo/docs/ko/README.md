# Description
### Molfinder
Molfinder는 <b>bank</b>에 임의의 화합물들을 넣고, Score가 낮은 화합물들을 <b>seed</b>로 넣고 seed와 bank사이에서 Crossover와 Mutation을 진행하면서 새로운 화합물을 찾습니다.
![image](https://github.com/arontier/ad3-descs/assets/98073046/d504a64b-e38a-4376-ba42-3deb2594de52)


---
# Inputs
### Choose weighted models
 - TSV : Docking summary file or pIC50
   - head columns에 SMAILES (or CANON_SMILES), AK_E(or BINDING_E or SCORE)가 있어야 합니다.
   - AK_E, BIDNDING_E, SCORE가 같이 있다면 AK_E, BINDING_E, SCORE 순으로 우선 순위가 있습니다.
   - SCORE는 높을수록 좋음, AK_E와 BINDING_E가 낮을수록 좋습니다.

### Choose weighted method
 - QED : quantitative estimate of drug-likeness
 - J-Score : logP - SAscore -Ring penalty - Size penalty
 - Drug score : Drug score made with DMPNN model

#### weight : 높을 수록 해당 Score의 비율이 높아집니다.

### Penalties : 해당 조건에 맞아야 합니다.
 - Lipinski : Lipinski's rule of five, MW <= 550, HBD <= 5, HBA <= 10, logP <= 5 
 - Spiro : Spiro Atoms <= 1
 - Bridgehead : Bridgehead = 0
 - Ring : Ring 크기 5 or 6
 - Logp : lopg <= 6.5
 - SA : SAscore <= 3.5
 - Nring : Ring 갯수 <= 4
 - Hetero : Hetero Atom (C가 아닌 heavy atom) 수 <= 8
 - PAINS : PAINS filter = 0
 - Brenk : Brenk filter = 0
 - NIH : NIH fitler = 0

---
# Outputs
## Web page
### Summary
생성된 화합물의 id, Score, MW, QED, logP, Smiles

### Results
각 weighted와 Score에 대한 Histogram

## Download File
 - MF-reuslt.tsv : Summary file
 - MF-result.smi : Smiles file


---
# References
1. Kwon, Y.; Lee, J. MolFinder: An Evolutionary Algorithm for the Global Optimization of Molecular Properties and the Extensive Exploration of Chemical Space Using SMILES. J. Cheminform. 2021, 13 (1), 24.
2. G. R. Bickerton, G. V. Paolini, J. Besnard, S. Muresan and A. L. Hopkins, Quantifying the chemical beauty of drugs Nat. Chem., 2012, 4, 90–98.
