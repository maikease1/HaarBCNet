# Kvasir-SEG

## Download

- Official dataset page: [Kvasir-SEG](https://datasets.simula.no/kvasir-seg/)
- Download **Kvasir-SEG**, not the multi-class Kvasir dataset. Author-maintained alternative: [Kvasir-SEG repository](https://github.com/DebeshJha/Kvasir-SEG).

Dataset images, masks and archives are **not included** in this GitHub repository. Download them directly from the provider and follow its access, attribution and usage conditions. Public access does not transfer ownership of the data to this project.

## Local preparation

The source dataset contains `images/` and `masks/` with matched filenames. Preserve a reversible filename mapping if using numbered project IDs.

The HaarBCNet training data layout is:

```text
kvasir/
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
