# Datasets

This directory documents the five datasets used by HaarBCNet. **Only instructions are tracked here; no dataset images, masks or archives are uploaded.**

| Dataset | Local folder | Download source |
|---|---|---|
| [ISIC 2018](isic/README.md) | `isic/` | [Official page](https://challenge.isic-archive.com/data/) |
| [BUSI](busi780/README.md) | `busi780/` | [Official page](https://scholar.cu.edu.eg/?q=afahmy/pages/dataset) |
| [GlaS](glas/README.md) | `glas/` | [Official page](https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest/) |
| [CVC-ClinicDB](cvc-clinicdb/README.md) | `cvc-clinicdb/` | [Official page](https://polyp.grand-challenge.org/CVCClinicDB/) |
| [Kvasir-SEG](kvasir/README.md) | `kvasir/` | [Official page](https://datasets.simula.no/kvasir-seg/) |

1. Open the individual README and obtain data from the provider.
2. Follow the stated filename and mask-preparation guidance.
3. Point the training configuration to the prepared local dataset root.
4. Follow the original dataset terms and cite the dataset authors.

The folder names match the project dataset identifiers. Provider access requirements may include registration. Downloading and reorganizing data does not establish the exact train/validation/test split used in the paper.
