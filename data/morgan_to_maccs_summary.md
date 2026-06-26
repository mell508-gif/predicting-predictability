# Morgan → MACCS Cross-Representation Autoencoder

## Setup
- Input: 2048-bit Morgan fingerprints
- Target: 167-bit MACCS keys
- Latent dimension: 32
- Split: 70% train / 15% validation / 15% test
- Loss: Binary cross-entropy

## Experiments
| Model | Best validation BCE | Best epoch | Test BCE |
|---|---:|---:|---:|
| Baseline | 0.053087 | 16 | 0.051747 |
| Dropout (p=0.1) | 0.043607 | 50 | 0.041517 |
| Input masking noise (5%) | 0.049183 | 20 | Not evaluated |

## Best model
The dropout model performed best on validation and test data.

- Test bitwise accuracy: 98.4114%
- Mean per-molecule PR-AUC: 0.9892
- Mean per-molecule Tanimoto similarity: 0.9488

## Key files
- Notebook: `data/objective_3_lincs_morgan_autoencoder.ipynb`
- Results table: `data/morgan_to_maccs_latent32_results_summary.csv`
- Best dropout model: `models/morgan_to_maccs_latent32_dropout01_best.pt`
- Baseline curve: `figures/morgan_to_maccs_latent32_bce_curve.png`
- Dropout curve: `figures/morgan_to_maccs_latent32_dropout01_bce_curve.png`
- Noise curve: `figures/morgan_to_maccs_latent32_masknoise05_bce_curve.png`
