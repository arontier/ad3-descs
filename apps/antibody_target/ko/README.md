# Description 

안티바티 타겟 인터엑션은 아론티어에서 개발한 항체와 항원의 결합 여부를 예측하는 모델입니다. 이 인공지능 모델은 단백질 언어모델과 transformer를 활용한 결과물을 CNN으로 분석하여 항원고 항체 결합여부를 예측합니다. 

# Inputs

1. 항체의 중사슬 서열 (fasta format)
2. 항체의 경사슬 서열 (fasta format)
3. 항원 서열(들) (fasta format)

# Outputs

항원과 항체의 결합 여부를 0(결합하지 않음) 에서 1(결합함) 사의 확률로 예측합니다. 

# References
1. Xiaoyang Jing et al Single-sequence protein structure prediction by integrating protein language models PNAS 121:e2308788121 (2024) doi: 10.1073/pnas.2308788121
