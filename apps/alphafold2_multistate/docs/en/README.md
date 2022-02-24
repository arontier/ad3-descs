# Description 

MultiState Modeling is a method for predicting protein structure using Jumper J. et al method[1].
To generate various structural conformations of protein, Heo, L. and Feig, M. method were used.


# Inputs
* `Sequence` [EP00000014.fa](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/input/EP00000014.fa)


# Outputs

* model_1.pdb : Predicted Protein Structure (RCSB PDB Format)
* model_1.contact.png : It is a graph of the Residue-Residue Contact prediction result.
* model_1.contact.tsv : Contains Residue-Residue Contact prediction results.
* model_all.plddt.val.tsv :
* query.1.fa : Protein sequence used to predict structure.
* query.1.pdb_hits.hhr.gz
* query.1.uniref90_hits.sto.gz 
* query.1.uniref90_hits.txt.gz


# References

1. Jumper, J. et al. Highly accurate protein structure prediction with AlphaFold. Nature 1–11 (2021) doi:10.1038/s41586-021-03819-2.
2. Heo, L. & Feig, M. Multi-State Modeling of G-protein Coupled Receptors at Experimental Accuracy. Biorxiv 2021.11.26.470086 (2021) doi:10.1101/2021.11.26.470086.
