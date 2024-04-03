# Description 

안티바티 타깃 인터엑션은 아론티어에서 개발한 항체와 항원의 결합 여부를 예측하는 모델입니다. 이 인공지능 모델은 단백질 언어모델과 트랜스포머(transformer)를 활용한 결과물[1]을 CNN으로 분석하여 항원과 항체 결합여부를 예측하며 기존 모델(AbAgIntPre)[2] 보다 더 좋은 성능을 나타냅니다. 

![image (35)](https://github.com/arontier/ad3-tutorials/assets/121647082/61817e5d-9fca-4859-aadb-ace3b7ab05c9)

# Inputs

1. 항체의 중사슬 서열 (fasta format)
2. 항체의 경사슬 서열 (fasta format)
3. 항원 서열(들) (fasta format)

# Outputs

1. 항체와 항원의 결합 여부를 0(결합하지 않음) 에서 1(결합함) 사의 확률로 예측
2. 항체의 파라토프(paratope)와 항원의 에피토프(epitope)을 예측

# References
1. Xiaoyang Jing et al Single-sequence protein structure prediction by integrating protein language models PNAS 121:e2308788121 (2024) doi: 10.1073/pnas.2308788121
2. Yan Huang et al AbAgIntPre: A deep learning method for predicting antibody-antigen interactions based on sequence information Frontiers in Immunology 13:1053617 (2022) doi: 10.3389/fimmu.2022.1053617
