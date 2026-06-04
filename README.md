# Predicting Predictability

This repository contains code and notes for the summer research project on predicting the predictability of bioactive compounds from chemical structure.

# Current progress

Objective 2 focuses on molecular representation and feature engineering. So far, I have set up an RDKit workflow that converts SMILES strings into binary molecular fingerprints.

Current files:
- `notebooks/objective_2_rdkit_fingerprints.ipynb`: initial RDKit notebook for converting SMILES into Morgan fingerprints
- `data/example_morgan_fingerprints.csv`: small example output using ethanol, aspirin, caffeine, and ibuprofen

# Next steps

The next step is to apply this workflow to Perturb-Seqr's `drug_master.json` file, extract compounds with available SMILES strings, and generate binary RDKit representations for all valid compounds.
