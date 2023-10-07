# Description 

GalaxyDock3 is a protein–ligand docking program which considers the full ligand conformational flexibility by explicitly sampling the ligand ring conformation and allowing the relaxation of the full ligand degrees of freedom, including bond angles and lengths. This method is based on the previous version (GalaxyDock2) which performs the global optimization of a designed score function. Ligand ring conformation is sampled from a ring conformation library constructed from structure databases. The GalaxyDock3 score function was trained with an additional bonded energy term for the ligand on a large set of complex structures. The performance of GalaxyDock3 was improved compared to GalaxyDock2 when predicted ligand conformation was used as the input for docking, especially when the input ligand conformation differs significantly from the crystal conformation. GalaxyDock3 also compared favorably with other available docking programs on two benchmark tests that contained diverse ligand rings.

# Inputs

* `Receptor` [2gl0\_receptor.pdb](https://docs.ad3.io/media/apps/galaxydock3/examples/input/2gl0_receptor.pdb)
* `Ligand` [2gl0\_corina.mol2](https://docs.ad3.io/media/apps/galaxydock3/examples/input/2gl0_corina.mol2)

# Outputs

# References
