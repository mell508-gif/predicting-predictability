# Predicting the Predictability of Bioactive Compounds

This project investigates whether the predictability of a compound's transcriptional response can itself be predicted from chemical structure.

The workflow combines molecular representations, transcriptional signatures, and experimental context to generate compound-level (proxy, reconstruction-based) predictability scores, then tests whether those scores can be predicted from structure alone using a regression model. 

## Workflow

1. Learn compound representations from molecular fingerprints.
2. Learn transcriptional signature representations.
3. Combine compound, signature, and experimental context in a multimodal model to estimate predictability. Use reconstruction error to generate compound-level proxy predictability scores. 
4. Predict compound-level predictability from chemical structure using Extra Tress regression and analyze patterns by mechanism of action and structural scaffold.

## Repository

- `notebooks/final/` — final analysis notebooks
- `notebooks/archive/` — earlier exploratory notebooks
- `data/` — datasets and generated analysis outputs
- `models/` — trained models and model evaluation files
- `figures/` — figures generated throughout the analysis

See `notebooks/README.md` for the notebook order and instructions.
