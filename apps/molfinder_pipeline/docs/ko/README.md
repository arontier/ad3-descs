# Description

Molfinder와 Docking을 통해 목표 단백질과 결합세기가 강한 분자를 찾아 생성합니다.

De novo와 Sacffold로 나누어지며 De novo는 새로운 ligand를 생성하고, scaffold는 분자의 scaffold를 기반으로 R group에 변화를 주며 새로운 ligand를 생성한다.

# Inputs

- `Target` [ASK1.6OYT.A_protein.pdb](https://openapi.ad3.io/media/apps/molfinder_pipeline/examples/input/ASK1.6OYT.A_protein.pdb)

결합 세기를 예측하기 위한 Docking summary file

- `Model` [sample_data.tsv](https://openapi.ad3.io/media/apps/molfinder_pipeline/examples/input/sample_data.tsv)

추가로 다른 특성을 예측하기 위한 Chembl pChEMBL file

- `Model` [ASK1_chembl.tsv](https://openapi.ad3.io/media/apps/molfinder_pipeline/examples/input/ASK1_chembl.tsv)

# Outputs

# References
