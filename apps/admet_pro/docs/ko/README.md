# Description

분자의 ADMET에 대해서 계산합니다.

---

# Inputs
## Query compounds
- Drawing : 2D로 화합물을 그리고 Import drawings을 누르면 smiles로 입력됩니다.
- Smiles : Smiles와 이름을 넣어주세요.

---
# Outputs
## Web page
### Summary
|ADMET|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|:-:|
| Toxicity | MCF | Medicinal Chemistry Filter |Count|Less is better|
| Toxicity | GLAXO | Glaxo Wellcome: Hard Filters |Count|Less is better|
| Toxicity | DUNDEE | University of Dundee: NTD Screening Library |Count|Less is better|
| Toxicity | BMS | BMS: HTS Deck Filters|Count|Less is better|
| Toxicity | PAINS | Pan Assay Interference Compounds (PAINS) |Count|Less is better|
| Toxicity | SureChEMBL | - |Count|Less is better|
| Toxicity | MLSMR | NIH MLSMR: Excluded Functionality Filters |Count|Less is better|
| Toxicity | Inpharmatica | Inpharmatica: Unwanted Fragments |Count|Less is better|
| Toxicity | LINT | Pfizer: Lint procedure |Count|Less is better|
| Metabolism | CYP1A2 | CYP1A2 inhibitor | - or + |- is better|
| Metabolism | CYP2C9 | CYP2C9 inhibitor | - or + |- is better|
| Metabolism | CYP2C19 | CYP2C19 inhibitor | - or + |- is better|
| Metabolism | CYP2D6 | CYP2D6 inhibitor | - or + |- is better|
| Metabolism | CYP3A4 | CYP3A4 inhibitor | - or + |- is better|
|Distribution| BBB | Blood-brain barrier Pennetration | - or + |not pass or pass|
| Toxicity | AGONIST| androgen receptor(AR) agonist | - or +| not agonist or agonist|
| Toxicity| hERG | Cardiotoxicity|- or +| not toxic or toxic|
| Toxicity| DILI|Drug Induced Liver Injury|- or +|not toxic or toxic|
| Toxicity|NEURO|Neurotoxicity|- or +|not toxic or toxic|

- CYP의 경우 0-0.1(---), 0.1-0.3(--), 0.3-0.5(-), 0.5-0.7(+), 0.7-0.9(++), and 0.9-1.0(+++).

### Histogram
RF_filter와 다른 나머지 ADMET의 Histogram입니다.

RF_filter : MCF, GLAXO, DUNDEE, BMS, PAINS, SureChEMBL, MLSMR, Inpharmarica, LINT

- Drug like : 모든 필터가 0
- Semi Drig like : 모든 필터의 합이 6 이하
- No Drog like : 모든 필터의 합이 6 초과

## Download File
- ADMET_summary.tsv : Summary 파일입니다.


# References
1. Shaker, B., Lee, J., Lee, Y., Yu, M. S., Lee, H. M., Lee, E., et al. A machine learning-based quantitative model (LogBB_Pred) to predict the blood–brain barrier permeability (logBB value) of drug compounds Bioinformatics 39 (10), btad577. 2023
2. Yu MS, Lee J, Lee Y, Na D (2020) 2-D chemical structure image-based in silico model to predict agonist activity for androgen receptor. BMC Bioinform 21(5):245
3. Lee, J.; Yu, M.-S.; Na, D. DILI-Stk: An Ensemble Model for the Prediction of Drug-induced Liver Injury of Drug Candidates. Curr. Bioinf. 2022, 17, 296– 303,
