# Description

### Reverse docking
하나의 화합물을 여러 단백질에 Docking하여 ligand 결합 에너지를 측정하는 방법이다. \
화합물에 대해 잠재적으로 결합하는 단백질을 식별할 수 도 있고, 약물의 독성에 대해서 알아보는데 사용되기도 합니다.

### Fittest
 여러 화합물들에 대한 공통 또는 동시에 Target 되는 단백질을 찾는 방법이다. \
 화합물들 마다 결합된 단백질의 score를 Z-score로 표준화하고 Z-score의 합산을 통해 ligand들에 가장 결합 가능성이 높은 단백질을 찾는다. 

### Database
 3가지 데이터 베이스 (RCSB PDB, AlphFold DB, Uniprot)에서 단백질 구조들를 가져왔습니다. \
 알려진 binding site는 PLIP으로 정리하고, 3가지의 binding Site 예측프로그램들 (P2Rank, Fpocket, DeeSurf)로 단백질 구조에 대해서 계산하였습니다. \
 마지막으로 binding site들을 클러스터링하여 단백질 구조와 binding site 데이터 베이스를 만들었습니다. 

<img src="https://github.com/arontier/ad3-descs/assets/98073046/dc7cad49-3733-4bc1-885b-4c7af2439b2b" width="70%" height="70%">

### Method
* Docking : Autodock-GPU
* Scoreing : AK-Score2, Z-score

---------------------
# Inputs
### Ligands
 - Ligands : sdf 또는 pdb 파일을 넣을 수 있습니다.

   pdb는 CONECT를 포함되어야 정확한 분자 결합이 표현됩니다.
### Similar ligand
ZINC20 Database에서 similarity가 0.8 이상인 화합물을 찾고 Ligands의 갯수가 10개가 될 때까지 추가합니다.(10개가 안될 수도 있습니다.)

---------------------
# Outputs
## Web page
### Target
화합물들의 Molecule Weight (MW), logP, Hydrogen bond donor (HBD), Hydrogen bond acceptor (HBA), TPSA, QED, SMILES, 2D image입니다.

### Target analyze

 - 단백질의 Autodock energy와 AK-Score2 Enegy를 화합물 간에 상관관계를 Heatmap으로 그렸습니다.
 - 화합물 간의 관계를 Diversity tree로 나타냈습니다.

### Protein Candidates 
Z-Score Energy을 기준으로 상위의 단백질들과 분자들이 결합된 구조와 AK-Score2 Energy를 보여주고 있습니다.


## Download File
 - Reverse_Dock.target.tsv : 입력한 Target에 대한 정보입니다.
 - Reverse_Dock.summary.tsv : 결과 테이블로 UNIPROT_ID, POCKET_ID, GENE_NAME, LIG_ID, AK_E가 있습니다.
 - Reverse_Dock.zscore.tsv : UNIRPOT_ID와 zscore의 평균 그리고 zscore의 순위가 있습니다.
 - zscore_pdbs.tgz : 상위의 단백질과 결합하고 있는 화합물들의 구조들이 들어있는 압축파일입니다.
 - {name}.report.pdf : 정리된 PDF파일입니다.
 - {name}.report.xlsx : 정리된 excel파일입니다.
 - failed_ligands.tsv : Docking에 실패한 화합물과 이유입니다.
---------------------

# References
1. H.M. Berman, J. Westbrook, Z. Feng, G. Gilliland, T.N. Bhat, H. Weissig, I.N. Shindyalov, P.E. Bourne, The Protein Data Bank (2000) Nucleic Acids Research 28: 235-242
2. Varadi, M. et al. “AlphaFold Protein Structure Database in 2024: Providing structure coverage for over 214 million protein sequences.” Nucleic Acids Research, gkad1011 (2023).
3. UniProt: the Universal Protein Knowledgebase in 2023. Nucleic Acids Res. 51:D523–D531 (2023)
4. alentin S., Schreiber S., Haupt V.J., Adasme M.F., Schroeder M. PLIP: fully automated protein–ligand interaction profiler,Nucleic Acids Res. 2015 Jul 1; 43(W1): W443–W447.
5. Krivák R, Hoksza D. P2Rank: machine learning based tool for rapid and accurate prediction of ligand binding sites from protein structure. J Chem 2018;10:1–12.
6. Guilloux V.L., Schmidtke P., Tuffery P. Fpocket: an open source platform for ligand pocket detection. BMC Bioinformatics. 2009; 10:168.
7. Mylonas, S. K., Axenopoulos, A. & Daras, P. DeepSurf: a surface-based deep learning approach for the prediction of ligand binding sites on proteins. Bioinformatics 37, 1681–1690 (2021).
8. Diogo Santos-Martins, Leonardo Solis-Vasquez, Andreas F Tillack, Michel F Sanner, Andreas Koch, Stefano Forli. Accelerating AutoDock4 with GPUs and Gradient-Based Local Search J. Chem. Theory Comput. 2021, 17, 2, 1060–1073
9. Kwon Y, Shin WH, Ko J, Lee J. AK-Score: Accurate Protein-Ligand Binding Affinity Predㅑiction Using an Ensemble of 3D-Convolutional Neural Networks. Int. J. Mol. Sci. 2020, 21(22), 8424
