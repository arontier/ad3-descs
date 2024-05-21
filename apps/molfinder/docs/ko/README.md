# Description
### Molfinder-Scaffold
Molfinder-Scaffold는 입력된 scaffold를 기반으로 데이터베이스에 있는 fragment를 가져와 scaffold와 결합합니다. \
 기존 Molfinder의 operation이 fragment에서만 진행되며 fragment를 random으로 가져오는 selection을 추가되어 새로운 화합물을 찾습니다.
<img src="https://github.com/arontier/ad3-descs/assets/98073046/d504a64b-e38a-4376-ba42-3deb2594de52" width="70%" height="70%">

### Database
 - GDB-11(179,173,826) : 간단한 화학적 안정성과 합성 가능성 규칙에 따라 C, N, O, F의 원자 11개까지의 작은 유기 분자를 열거한 database입니다.
 - Library(367,063) : Mcule와 Enamine의 Fragment database입니다.
 - Enamine(2,993) : Essential Fragment Library,High Fidelity Fragment Library,DSI-poised Library in Enamine. Deduplicated
 - Mini(2,025) : Mcule와 Enamine의 mini fragment database로 heavy atoms이 7개 이하인 database입니다..

#### Mini and Enamine have no effect on the fragment size option.
#### For databases other than GDB-11, if the number of *'s is 1, it will fragment as much as possible and take the best.

---
# Inputs
### Query compound
 - Drawings : 화합물을 그리고 fragment를 붙이고 싶은 곳에 R을 넣고 <b>Import drawings</b>를 누르면 됩니다.
 - Samiles : 원하는 Scaffold를 넣고 fragment를 붙이고 싶은곳에 (*)을 넣으면 됩니다.

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
### Target
Scaffold의 Score, MW, QED, logP, Smiles 
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
3. Fink, T.; Reymond, J.-L. Virtual exploration of the chemical universe up to 11 atoms of C, N, O, F: assembly of 26.4 million structures (110.9 million stereoisomers) and analysis for new ring systems, stereochemistry, physico-chemical properties, compound classes and drug discovery. J. Chem. Inf. Model. 2007, 47, 342-353.
4. [Mcule database](https://mcule.com/database/)
5. [Enamine database](https://enamine.net/compound-libraries/fragment-libraries)
