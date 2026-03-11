# FordA Dataset Notes

Source:
- UCR/UEA style archive distribution (`FordA.zip`)
- Download URL used: https://www.timeseriesclassification.com/aeon-toolkit/FordA.zip

Files in this folder:
- `FordA_TRAIN.tsv`
- `FordA_TEST.tsv`

Format:
- Column 0: class label (`-1` or `1`)
- Columns 1..500: time-series values

Conversion done:
- Original `.txt` files were converted to tab-separated `.tsv` while keeping values unchanged.

Dataset size:
- Train: 3601 samples
- Test: 1320 samples
- Sequence length: 500

Experiment protocol used in this repository:
- Primary experiments keep FordA at full length 500.
- Early classification is measured on prefixes (10% to 100%) of the same 500-length series.
- Therefore, 100 points correspond to a 20% prefix, not to a truncated replacement dataset.
