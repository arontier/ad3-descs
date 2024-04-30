<!-- @format -->

# Description

분자의 다양한 특징에 대해서 계산합니다.
|Name|Description|Unit|Range or recommended values|
|:-:|:-:|:-:|:-:|
|MW|화합물 무게|g/mol|150 ~ 650|
|logP|극성 용매(물)와 비극송 용매(옥탄올) 사이의 물질 분포 계수||-5 ~ 5|
|HBD|수소결합 H Donor||<5|
|HBA|수소결합 H Acceptor||<10|
|TPSA|토폴로지 극성 표면적|Å|<140|
|QED|약물 유사성 정량화||0~1(Best)|
|SAScore|합성 가능성 예측||(Best)0~10|
|SYBA|합성 접근성에 대한 베이지안 추정||-100~100(best)|
|RAScore|역합성 가능성 예측||0~1(Best)|
|ESOL|예상 용해도|||

Filter는 원하는 property (MW, logp, HBD, HBA, TPSA)를 가진 분자를 따로 뽑습니다.

# Inputs

- `Query Compounds` [sample.smi](https://openapi.ad3.io/media/apps/property/examples/input/sample.smi)

# Outputs

- `property_summary` [property_summary.tsv](https://openapi.ad3.io/media/apps/property/examples/output/property_summary.tsv)
- `property_filter` [property_filter.tsv](https://openapi.ad3.io/media/apps/property/examples/output/property_filter.tsv)

# References

- G. Richard Bickerton, Quantifying the chemical beauty of drugs. Nature Chemistry volume 4, 90–98 (2012)
- Peter Ertl, Estimation of synthetic accessibility score of drug-like molecules based on molecular complexity and fragment contributions. J. Cheminformatics 1, 8(2009)
- Milan Voršilák, SYBA: Bayesian estimation of synthetic accessibility of organic compounds. J. Cheminformatics 12, 35(2020)
- Amol Thakkar, Retrosynthetic accessibility score (RAscore) – rapid machine learned synthesizability classification from AI driven retrosynthetic planning. Chem. Sci. 9, 2021
