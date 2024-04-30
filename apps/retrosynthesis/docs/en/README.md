# Description

We recast the retrosynthetic planning problem as a language translation problem using a template-free sequence-to-sequence model. The model is trained in an end-to-end and a fully data-driven fashion. Unlike previous models translating the SMILES strings of reactants and products, we introduced a new way of representing a chemical reaction based on molecular fragments. It is demonstrated that the new approach yields better prediction results than current state-of-the-art computational methods. The new approach resolves the major drawbacks of existing retrosynthetic methods such as generating invalid SMILES strings. Specifically, our approach predicts highly similar reactant molecules with an accuracy of 57.7%. In addition, our method yields more robust predictions than existing methods.

# Inputs

- `Compound` [example.smi](https://openapi.ad3.io/media/apps/retrosynthesis/examples/input/example.smi)

# Outputs

# References

- Ucak, U. V., Kang, T., Ko, J. & Lee, J. Substructure-based neural machine translation for retrosynthetic prediction. J Cheminformatics 13, 4 (2021). \[[Journal]\](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-020-00482-z) \[[Pubmed]\](https://pubmed.ncbi.nlm.nih.gov/33431017/)
- Ucak, U. V., Ashyrmamatov, I., Ko, J. & Lee, J. RetroTRAE: retrosynthetic translation of atomic environments with Transformer. doi:10.33774/chemrxiv-2021-9g274.
