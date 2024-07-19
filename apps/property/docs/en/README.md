<!-- @format -->

# Description

Calculate properties a molecule.

---


# Inputs
### Query compounds
 - Drawing : If you draw the compound in 2D and hit Import drawings, it will be entered as smiles.
 - Smiles : Add Smiles and name.

### Apply Filter
Select a range for the five properties and find the compounds that fit within it.

---
# Outputs
## Web page
### Molecule Summary
|  Name   |                  Description                   | Unit  | Range or recommended values |
| :-----: | :--------------------------------------------: | :---: | :-------------------------: |
|   MW    |                Molecular weight                | g/mol |          150 ~ 650          |
|  logP   |       octanol/water partition coefficient       |       |           -5 ~ 5            |
|   HBD   |              Hydrogen bond Donor               |       |             <5              |
|   HBA   |             Hydrogen bond Acceptor             |       |             <10             |
|  TPSA   |         Topological polar surface area         |   Å   |            <140             |
|   QED   |    Quantifying the chemical beauty of drugs    |       |          0~1(Best)          |
| SAScore |         synthetic accessibility score          |       |         (Best)1~10          |
|  SYBA   | Bayesian estimation of synthetic accessibility |       |       -100~100(best)        |
| RAScore |       Retrosynthetic accessibility score       |       |          0~1(Best)          |
|  ESOL   |         Estimating aqueous solubility          |       |                             |

### Histogram
Histogram of each property.

## Download File
- property_summary.tsv : Summary file.
- property_filte : Compounds that fit the fiter condition.

# References

- G. Richard Bickerton, Quantifying the chemical beauty of drugs. Nature Chemistry volume 4, 90–98 (2012)
- Peter Ertl, Estimation of synthetic accessibility score of drug-like molecules based on molecular complexity and fragment contributions. J. Cheminformatics 1, 8(2009)
- Milan Voršilák, SYBA: Bayesian estimation of synthetic accessibility of organic compounds. J. Cheminformatics 12, 35(2020)
- Amol Thakkar, Retrosynthetic accessibility score (RAscore) – rapid machine learned synthesizability classification from AI driven retrosynthetic planning. Chem. Sci. 9, 2021
