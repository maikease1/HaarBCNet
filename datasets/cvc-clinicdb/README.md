# CVC-ClinicDB

## Download

- Official dataset page: [CVC-ClinicDB](https://polyp.grand-challenge.org/CVCClinicDB/)
- Obtain the CVC-ClinicDB images and ground-truth masks from the official challenge page. Alternative institutional entry: [CVC-Colon databases](https://pages.cvc.uab.es/CVC-Colon/index.php/databases/). Access may require following the provider's current registration instructions.

Dataset images, masks and archives are **not included** in this GitHub repository. Download them directly from the provider and follow its access, attribution and usage conditions. Public access does not transfer ownership of the data to this project.

## Local preparation

Pair every image with its ground-truth mask. Preserve the original filenames or record an explicit ID mapping when reorganizing the TIFF files.

The HaarBCNet training data layout is:

```text
cvc-clinicdb/
├── images/
│   └── <sample_id>.<image_extension>
├── masks/
│   └── 0/
│       └── <sample_id>.<mask_extension>
└── edges/                  # optional: masks can be used to derive boundary targets
    └── 0/
        └── <sample_id>.<edge_extension>
```

Configure `data_root`, `img_ext` and `mask_ext` to match your prepared files. Keep original images and masks locally; do not commit them. The image and its mask must share the same sample ID. Reorganizing files alone does not reproduce the paper split; use the experiment-specific split ID files when reproducing reported results.

See the [dataset overview](../README.md). Download information checked on 2026-11-06; provider links or access requirements may change.
