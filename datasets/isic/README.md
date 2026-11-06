# ISIC 2018

## Download

- Official dataset page: [ISIC 2018](https://challenge.isic-archive.com/data/)
- Choose **2018 → Task 1: Lesion Boundary Segmentation**. Download the training input images and Task 1 ground-truth segmentation masks. Do not substitute Task 2 attribute masks or Task 3 classification labels.

Dataset images, masks and archives are **not included** in this GitHub repository. Download them directly from the provider and follow its access, attribution and usage conditions. Public access does not transfer ownership of the data to this project.

## Local preparation

Input images use names such as `ISIC_<id>.jpg`; Task 1 masks commonly use `ISIC_<id>_segmentation.png`. Image/mask stems must be mapped consistently when preparing the training layout.

The HaarBCNet training data layout is:

```text
isic/
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
