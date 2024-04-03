# Description 

안티바디폴딩은 Evans R J. et al의 방법[1, 2]을 활용하여 항체 3차원 구조를 예측하는 방법입니다. 항체의 중사슬과 경사슬의 서열을 입력하면 항체 3차원 구조를 예측할 수 있습니다. 아래 예제 항체 입력서열은 Colton J Bracken et al[3]의 항 ACE3 항체 서열입니다. 
# Inputs

\>Heavy_chain 
<br>
EVQLVQSGPEVKKPGTSVKVSCKASGFTFMSSAVQWVRQARGQRLEWIGWIVIGSGNTNYAQKFQERVTITRDMSTSTAYMELSSLRSEDTAVYYCAAPYCSSISCNDGFDIWGQGTMVTVS 
<br>
\>Light_chain 
<br>
DVVMTQTPFSLPVSLGDQASISCRSSQSLVHSNGNTYLHWYLQKPGQSPKLLIYKVSNRFSGVPDRFSGSGSGTDFTLKISRVEAEDLGVYFCSQSTHVPYTFGGGTKLEIK <br>

# Outputs

중사슬과 경사슬을 포함한 항체 3차원 구조

![스크린샷, 2024-04-02 13-49-29](https://github.com/arontier/ad3-tutorials/assets/121647082/1b4fa9ab-da29-420f-9933-98bf02a45a94)


# References

1. Evans, R et al. Protein complex prediction with AlphaFold-Multimer bioRxiv (2022) doi: https://doi.org/10.1101/2021.10.04.463034
2. https://github.com/google-deepmind/alphafold/blob/main/docs/technical_note_v2.3.0.md
3. Colton J Bracken et al. Bi-paratopic and multivalent VH domains block ACE2 binding and neutralize SARS-CoV-2 Nat Chem Biol . 17:113-121 (2021) doi: 10.1038/s41589-020-00679-1
