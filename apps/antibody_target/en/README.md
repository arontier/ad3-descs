# Description 

Antibody-Antigen Interaction is developed by Arontier Co. for predicting the probability of interaction between antibodies and antigens. This model incorporates outputs from a protein language model and a transformer, which are then utilized in a convolutional neural network (CNN) module (ATI module) to calculate binding probabilities, as described in the figure below. It has been observed that this model outperforms the recent AbAgInterPre model, which is another antibody-antigen interaction prediction model.

![image (35)](https://github.com/arontier/ad3-tutorials/assets/121647082/71f943c2-be1a-414f-9fee-820e5d0409f4)

# Inputs

1. The fasta sequence of the antibody heavy chain within 150 a.a.

\>Heavy_Ab
QVQMQQPGAELVKPGASVKLSCKASGYTFISYWMHWVKQRPGRGLEWIGRIAPDTGIIYYNEKFKNKATLTVDTPSSTAYMQLNSLTSEDSAVYYCARYLKYDGSTYRFDYWGQGTTLTV

2. The fasta sequence of the antibody light chain within 150 a.a.

\>Light_Ab
DIVMTQAAPSVPVTPGESVSISCRSSKSLLHSNGNTYLFWFLQRPGQSPQLLIYRMSNLASGVPDRFSGSGSGTSFTLRISRVEAEDVGVYYCMQHLEYPYTFGGGTKLEIKRADAAPTV

3. The fasta sequence of the antigen  within 300 a.a.

\>Antigen
GGGGVAADIGAGLADALTAPLDHKDKGLQSLTLDQSVRKNEKLKLAAQGAEKTYGNGDSLNTGKLKNDKVSRFDFIRQIEVDGQLITLESGEFQVYKQSHSALTAFQTEQIQDSEHSGKMVAKRQFRIGDIAGEHTSFDKLPEGGRATYRGTAFGSDDAGGKLTYTIDFAAKQGNGKIEHLKSPELNVDLAAADIKPDGKRHAVISGSVLYNQAEKGSYSLGIFGGKAQEVAGSAEVKTVNGIRHIGL

# Outputs

1. Interaction probability
2. Predicted epitopes ans paratopes

# References

1. Xiaoyang Jing et al Single-sequence protein structure prediction by integrating protein language models PNAS 121:e2308788121 (2024) doi: 10.1073/pnas.2308788121
2. Yan Huang et al AbAgIntPre: A deep learning method for predicting antibody-antigen interactions based on sequence information Frontiers in Immunology 13:1053617 (2022) doi: 10.3389/fimmu.2022.1053617
