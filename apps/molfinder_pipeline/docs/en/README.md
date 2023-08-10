# Description 
목표 단백질과 binding energy가 최소가 되는 새로운 ligand를 생성하는 모델.

De novo와 Sacffold로 나누어지며 De novo는 새로운 ligand를 생성하고, scaffold는 분자의 scaffold를 기반으로 R group에 변화를 주며 새로운 ligand를 생성한다.
# Inputs

* `Target` [ASK1.6OYT.A_protein.pdb](https://docs.ad3.io/media/apps/molfinder_pipeline/examples/input/ASK1.6OYT.A_protein.pdb)


결합 세기를 예측하기 위한 Docking summary file
* `Model` [sample_data.tsv](https://docs.ad3.io/media/apps/molfinder_pipeline/examples/input/sample_data.tsv)

추가로 다른 특성을 예측하기 위한 Chembl pChEMBL file
* `Model` [sample_data.tsv](https://docs.ad3.io/media/apps/molfinder_pipeline/examples/input/ASK1_chembl.tsv)

# Outputs


# References
