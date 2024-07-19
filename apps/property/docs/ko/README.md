<!-- @format -->

# Description

분자의 다양한 속성에 대해서 계산합니다. 

---

# Inputs
### Query compounds
- Drawing : 2D로 화합물을 그리고 Import drawings을 누르면 smiles로 입력됩니다.
- Smiles : Smiles와 이름을 넣어주세요.

### Apply Filter
5가지의 속성(MW, logp, HBD, HBA, TPSA)에 대해서 조건에 맞는 분자를 따로 뽑습니다.

---
# Outputs
## Web page
### Molecule Summary
|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|
|MW|화합물 무게|g/mol|150 ~ 650|
|logP|극성 용매(물)와 비극송 용매(옥탄올) 사이의 물질 분포 계수||-5 ~ 5|
|HBD|수소 결합 주개(Hydrogen bond donor)||<5|
|HBA|수소 결합 받개 (Hydrogen bond acceptor)||<10|
|TPSA|토폴로지 극성 표면|Å|<140|
|QED|약물 유사성 정량화||0~1(Best)|
|SAScore|합성 가능성 예측||(Best)1~10|
|SYBA|합성 접근성에 대한 베이지안 추정||-100~100(best)|
|RAScore|역합성 가능성 예측||0~1(Best)|
|ESOL|예상 용해도|||

### Histogram
각 속성들의 Histogram

## Download File
- property_summary.tsv : Summary 파일입니다.
- property_filter : fiter 조건에 맞는 화합물들입니다.

---
# References

- G. Richard Bickerton, Quantifying the chemical beauty of drugs. Nature Chemistry volume 4, 90–98 (2012)
- Peter Ertl, Estimation of synthetic accessibility score of drug-like molecules based on molecular complexity and fragment contributions. J. Cheminformatics 1, 8(2009)
- Milan Voršilák, SYBA: Bayesian estimation of synthetic accessibility of organic compounds. J. Cheminformatics 12, 35(2020)
- Amol Thakkar, Retrosynthetic accessibility score (RAscore) – rapid machine learned synthesizability classification from AI driven retrosynthetic planning. Chem. Sci. 9, 2021
