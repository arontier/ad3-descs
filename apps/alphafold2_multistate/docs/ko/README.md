# Description 

Monomer는 단백질의 서열로부터 3차원 구조를 예측하는 방법입니다. AlphaFold[1], Multi-State Modeling[2] 등 다양한 구조 예측 방법을 단일 앱에서 사용할 수 있도록 개발되었으며, ad3에서 최적화한 구조 예측 방법을 추가로 제공합니다.


# Examples

## Multi-State Modeling

* MAPK14 [AD3XX00000152](https://www.ad3.io/pub-targets/152)
* Conformational States
  * DFGin-BLAminus : 1wbw_A,3hvc_A,6tca_B,6tca_D,6tca_F,6tca_H,6zqs_A
* Sequence
```
>MAPK14
MSQERPTFYRQELNKTIWEVPERYQNLSPVGSGAYGSVCAAFDTKTGLRVAVKKLSRPFQSIIHAKRTYRELRLLKHMKHENVIGLLDVFTPARSLEEFNDVYLVTHLMGADLNNIVKCQKLTDDHVQFLIYQILRGLKYIHSADIIHRDLKPSNLAVNEDCELKILDFGLARHTDDEMTGYVATRWYRAPEIMLNWMHYNQTVDIWSVGCIMAELLTGRTLFPGTDHIDQLKLILRLVGTPGAELLKKISSESARNYIQSLTQMPKMNFANVFIGANPLAVDLLEKMLVLDSDKRITAAQALAHAYFAQYHDPDDEPVADPYDQSFESRDLLIDEWKSLTYDEVISFVPPPLDQEEMES
```


# Outputs

* [model_1.pdb](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/model_1.pdb) : Predicted Protein Structure (RCSB PDB Format)
* [model_1.contact.png](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/model_1.contact.png) : It is a graph of the Residue-Residue Contact prediction result.
* [model_1.contact.tsv](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/model_1.contact.tsv) : Contains Residue-Residue Contact prediction results.
* [model_all.plddt.val.tsv](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/model_all.plddt.val.tsv)
* [query.1.fa](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/query.1.fa) : Protein sequence used to predict structure.
* [query.1.pdb_hits.sto.gz](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/query.1.pdb_hits.sto.gz)
* [query.1.uniref90_hits.sto.gz](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/query.1.uniref90_hits.sto.gz)
* [query.1.uniref90_hits.txt.gz](https://docs.ad3.io/media/apps/alphafold2_multistate/examples/output/download/query.1.uniref90_hits.txt.gz)


# References

1. Jumper, J. et al. Highly accurate protein structure prediction with AlphaFold. Nature 1–11 (2021) doi:10.1038/s41586-021-03819-2.
2. Heo, L. & Feig, M. Multi‐state modeling of G‐protein coupled receptors at experimental accuracy. Proteins Struct Funct Bioinform (2022) doi:10.1002/prot.26382.
3. Modi, V. & Dunbrack, R. L. Kincore: a web resource for structural classification of protein kinases and their inhibitors. Nucleic Acids Res 50, D654–D664 (2022).
4. Modi, V. & Dunbrack, R. L. Defining a new nomenclature for the structures of active and inactive kinases. P Natl Acad Sci Usa 116, 6818–6827 (2019).
