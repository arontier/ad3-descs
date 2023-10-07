# Description 

Monomer는 단백질의 서열로부터 3차원 구조를 예측하는 방법입니다. AlphaFold[1], Multi-State Modeling[2] 등 다양한 구조 예측 방법을 단일 앱에서 사용할 수 있도록 개발되었으며, ad3에서 최적화한 구조 예측 방법을 추가로 제공합니다.


# Examples

## Monomer Modeling

* MAPK14 [AD3XX00000152](https://www.ad3.io/pub-targets/152)
  * Sequence
```
>MAPK14
MSQERPTFYRQELNKTIWEVPERYQNLSPVGSGAYGSVCAAFDTKTGLRV
AVKKLSRPFQSIIHAKRTYRELRLLKHMKHENVIGLLDVFTPARSLEEFN
DVYLVTHLMGADLNNIVKCQKLTDDHVQFLIYQILRGLKYIHSADIIHRD
LKPSNLAVNEDCELKILDFGLARHTDDEMTGYVATRWYRAPEIMLNWMHY
NQTVDIWSVGCIMAELLTGRTLFPGTDHIDQLKLILRLVGTPGAELLKKI
SSESARNYIQSLTQMPKMNFANVFIGANPLAVDLLEKMLVLDSDKRITAA
QALAHAYFAQYHDPDDEPVADPYDQSFESRDLLIDEWKSLTYDEVISFVP
PPLDQEEMES
```

* IDH1 [AD3XX00000320](https://www.ad3.io/pub-targets/320)
```
>IDH1
MSKKISGGSVVEMQGDEMTRIIWELIKEKLIFPYVELDLHSYDLGIENRD
ATNDQVTKDAAEAIKKHNVGVKCATITPDEKRVEEFKLKQMWKSPNGTIR
NILGGTVFREAIICKNIPRLVSGWVKPIIIGRHAYGDQYRATDFVVPGPG
KVEITYTPSDGTQKVTYLVHNFEEGGGVAMGMYNQDKSIEDFAHSSFQMA
LSKGWPLYLSTKNTILKKYDGRFKDIFQEIYDKQYKSQFEAQKIWYEHRL
IDDMVAQAMKSEGGFIWACKNYDGDVQSDSVAQGYGSLGMMTSVLVCPDG
KTVEAEAAHGTVTRHYRMYQKGQETSTNPIASIFAWTRGLAHRAKLDNNK
ELAFFANALEEVSIETIEAGFMTKDLAACIKGLPNVQRSDYLNTFEFMDK
LGENLKIKLAQAKL%
```


## Multi-State Modeling

* MAPK14 [AD3XX00000152](https://www.ad3.io/pub-targets/152)
  * DFGin-BLAminus : 1wbw_A,3hvc_A,6tca_B,6tca_D,6tca_F,6tca_H,6zqs_A
  * DFGin-BLBminus : 1a9u_A,1bl6_A,1bl7_A,1bmk_A,1di9_A,1m7q_A,1ouk_A,1ouy_A,1oz1_A,1r39_A,1r3c_A,1w7h_A,1w84_A,1yqj_A,2lgc_A,2okr_A,2okr_D,2onl_A,2onl_B,2y8o_A,2zb0_A,2zb1_A,3flq_A,3fmj_A,3fsf_A,3mpa_A,3mw1_A,3zya_A,5eta_A,5eta_B,5etf_A,5n68_A,5xyx_A,5xyy_A


# References

1. Jumper, J. et al. Highly accurate protein structure prediction with AlphaFold. Nature 1–11 (2021) doi:10.1038/s41586-021-03819-2.
2. Heo, L. & Feig, M. Multi‐state modeling of G‐protein coupled receptors at experimental accuracy. Proteins Struct Funct Bioinform (2022) doi:10.1002/prot.26382.
3. Modi, V. & Dunbrack, R. L. Kincore: a web resource for structural classification of protein kinases and their inhibitors. Nucleic Acids Res 50, D654–D664 (2022).
4. Modi, V. & Dunbrack, R. L. Defining a new nomenclature for the structures of active and inactive kinases. P Natl Acad Sci Usa 116, 6818–6827 (2019).
