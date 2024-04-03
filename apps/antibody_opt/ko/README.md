# Description 

항체 최적화는 항원의 정보가 없어도 단백질언어모델을 통해 대다수의 진화된 항체서열이 다양한 항원에 대한 결합력이 향상된다는 실험적 검증을 바탕으로 [1] 항체의 결합력 항상된 점 돌연변이 서열을 예측합니다.
 
모든 가능한 점돌연변이 공간(full mutational space)에서 자연계에 가능성 높에 일어나는 점돌연변이 공간(Plausible mutation)은 결합력 향상시키는 점돌연변이 공간(Affinity-maturated mutation)의 많은 부분을 포함합니다. 언어모델에서 높은 가능성으로 생성된 점돌연변이(High language model likelihood)는 자연계에서 가능성 높게 일어나는 점돌연변이 공간보다(Plausible mutation) 보다 더 높은 확률로 결합력 향상시키는 점돌연변이 공간을 점유합니다(아래 그림 설명).       

![스크린샷, 2024-04-03 17-38-30](https://github.com/arontier/ad3-tutorials/assets/121647082/9c0688a0-e355-49ea-a1e3-330daa1fa6b3)



# Inputs

항체 단일 체인 서열


# Outputs

결합력이 향상된 것으로 예측되는 항체 단일 체인의 점 돌연변이 서열

# References

1. Hie BL et al. Efficient evolution of human antibodies from general protein language models. Nat Biotechnol. Feb 42(2):275-283 (2024) doi: 10.1038/s41587-023-01763-2
