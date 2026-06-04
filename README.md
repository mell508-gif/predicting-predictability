# Predicting Predictability

This repository contains code and notes for a summer research project on predicting how much the biological activity of bioactive compounds can be inferred from chemical structure.

# Project focus

The current phase of the project focuses on molecular representation and feature engineering. The goal is to convert compound structures into machine-readable feature tables that can later be compared for chemical similarity and predictive usefulness.

# Current progress

So far, I have built an RDKit-based workflow that converts SMILES strings into multiple molecular representations.

Completed steps:

- Set up a conda environment with RDKit.
- Tested the basic SMILES → RDKit molecule → fingerprint pipeline on a small example set of compounds.
- Loaded the Perturb-Seqr `drug_master.json` file locally.
- Converted 6,801 Perturb-Seqr compound records into a pandas dataframe.
- Generated Morgan fingerprints for valid compounds.
- Generated MACCS keys for valid compounds.
- Generated molecular descriptors for valid compounds.
- Began comparing representation tables by feature type, information captured, number of compounds, and number of columns.
- Began visualizing molecular descriptor distributions.

# Current files

# Notebooks

- `notebooks/objective_2_rdkit_fingerprints.ipynb`  
  Main notebook for loading Perturb-Seqr compound metadata, generating RDKit molecular representations, and beginning representation comparison.

# Data outputs

- `data/example_morgan_fingerprints.csv`  
  Small test output using ethanol, aspirin, caffeine, and ibuprofen.

- `data/perturbseqr_morgan_fingerprints.csv`  
  Morgan fingerprint feature table for Perturb-Seqr compounds.

- `data/perturbseqr_maccs_keys.csv`  
  MACCS key feature table for Perturb-Seqr compounds.

- `data/perturbseqr_molecular_descriptors.csv`  
  Molecular descriptor feature table for Perturb-Seqr compounds.

- `data/representation_comparison_summary.csv`  
  Summary table comparing the generated molecular representation tables.

# Figures

- `figures/`  
  Descriptor distribution plots for molecular weight, LogP, TPSA, hydrogen-bond donors/acceptors, rotatable bonds, aromatic rings, heavy atom count, and formal charge.

# Note on private data

The original `drug_master.json` file is not included in this repository because it came from a private Perturb-Seqr resource. The generated feature tables are included for review.

# Next steps

The next step is to compare fingerprint-based chemical similarity using Morgan fingerprints and MACCS keys. I plan to calculate Tanimoto/Jaccard similarity distributions for the same sample of compounds under both representations, then evaluate whether the two fingerprint methods organize chemical space differently.
