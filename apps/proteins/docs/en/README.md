# Description

A-Prot is a new protein 3D structure modeling method using MSA Transformer, one of the state-of-the-art protein language models. For a given MSA, an MSA feature tensor and row attention maps are extracted and converted into 2D residue-residue distance and dihedral angle predictions. We demonstrated that A-Prot predicts long-range contacts better than the existing methods. Additionally, we modeled the 3D structures of the free modeling and hard template-based modeling targets of CASP14. The assessment shows that the A-Prot models are more accurate than most top server groups of CASP14. These results imply that A-Prot captures evolutionary and structural information of proteins accurately with relatively low computational cost. Thus, A-Prot can provide a clue for the development of other protein property prediction methods.

# Inputs

- `Sequence` [DDR1.fa](https://openapi.ad3.io/media/apps/proteins/examples/input/DDR1.fa)

# Outputs

# References

- Hong, Y., Lee, J. & Ko, J. A-Prot: Protein structure modeling using MSA transformer. Biorxiv 2021.09.10.459866 (2021) doi:10.1101/2021.09.10.459866. [Journal](https://www.biorxiv.org/content/10.1101/2021.09.10.459866v1)
