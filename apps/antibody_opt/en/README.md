# Description 

Antibody optimization is a method used to predict the sequences of antibody chains that have undergone affinity maturation, without providing the model information about the target antigen, using the method proposed by Hie et al [1].

A language model, even without specific information about selection pressures, can still effectively guide antibody affinity maturation, as described in the figure below. 


![스크린샷, 2024-04-03 17-38-30](https://github.com/arontier/ad3-tutorials/assets/121647082/9115a480-a0f8-4971-a254-c8c211c0221d)


# Inputs

Antibody chain sequences 
\>Heavy_Fv
EVQLVQSGPEVKKPGTSVKVSCKASGFTFMSSAVQWVRQARGQRLEWIGWIVIGSGNTNYAQKFQERVTITRDMSTSTAYMELSSLRSEDTAVYYCAAPY
CSSISCNDGFDIWGQGTMVTVS

# Outputs

Outputs are point-mutated antibody chain sequences predicted as candidates with high affinity for certain antigens with a language model likelihood score. 

# References

1. Hie BL et al. Efficient evolution of human antibodies from general protein language models. Nat Biotechnol. Feb 42(2):275-283 (2024) doi: 10.1038/s41587-023-01763-2
