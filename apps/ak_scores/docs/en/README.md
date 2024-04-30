# Description

Accurate prediction of the binding affinity of a protein-ligand complex is essential for efficient and successful rational drug design. In this work, a new neural network model that predicts the binding affinity of a protein-ligand complex structure is developed. Our new model predicts the binding affinity of a complex using the ensemble of multiple independently trained networks that consist of multiple channels of 3D convolutional neural network layers. Our model was trained using the 3740 protein-ligand complexes from the refined set of the PDBbind database and tested using the 270 complexes from the core set. The benchmark results show that the correlation coefficient between the predicted binding affinities by our model and the experimental data is higher than 0.72, which is comparable with the state-of-the-art binding affinity prediction methods. In addition, our method also ranks the relative binding affinities of possible multiple binders of a protein quite accurately. Last, we measured which structural information is critical for predicting binding affinity.

# Inputs

- `Receptor` [MAP3K5.MULTIMODEL.protein.pdbqt](https://openapi.ad3.io/media/apps/ak_scores/examples/input/MAP3K5.MULTIMODEL.protein.pdbqt)
- `Ligand` [MAP3K5.MULTIMODEL.ligand.pdbqt](https://openapi.ad3.io/media/apps/ak_scores/examples/input/MAP3K5.MULTIMODEL.ligand.pdbqt)

# Outputs

# References
