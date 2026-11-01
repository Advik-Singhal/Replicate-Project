# Visual EEG ERP Replication Project

A Replicate project exploring how the brain's average electrical response changes when a person views different kinds of images. It uses the [Kaneshiro2015 dataset in MOABB](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Kaneshiro2015.html) to compare **event-related potentials (ERPs)**: EEG signals averaged across trials and aligned to the moment an image appears.

This is a descriptive exploration inspired by the original study, not a full reproduction of its classification or representational similarity analysis. It uses no classifier or machine learning.

## Research question

For one participant, how do average post-stimulus EEG responses compare for **human faces, animal faces, and inanimate objects**?

The notebook selects the first 60 trials per category, reconstructs the available 0–496 ms stimulus-locked epochs, and averages signals from 20 posterior sensors. It plots one ERP curve per category with trial-wise standard error bands.

## Run it in Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Advik-Singhal/Replicate-Project/blob/main/tks_kaneshiro2015_erp.ipynb)

1. Open the notebook using the button above and choose **Runtime → Run all**.
2. The first cell installs the required Python packages. The first data load downloads approximately **316 MB** for participant 1, so an internet connection is required.
3. Review the sensor selection, ERP comparison, and summary table. Run the cells in order if running them individually.

The notebook was executed successfully in a local Python environment using real data. The [executed notebook](tks_kaneshiro2015_erp_executed.ipynb) includes its plots and outputs for inspection without rerunning it.

## What the sample showed

All three averaged responses showed a positive deflection near **224 ms**. At that time, the human-face average was +0.127 µV, animal-face +0.118 µV, and inanimate-object +0.097 µV. These are descriptive observations from one participant and a small trial sample, not evidence of a statistically established category effect. See [FINDINGS.md](FINDINGS.md) for the full summary.

## Limitations

- One participant and 60 trials per condition cannot establish a result across people.
- The source data are already filtered, cleaned, average-referenced, and downsampled. The available epochs begin at stimulus onset, so this analysis has no prestimulus baseline.
- The posterior sensor group is chosen by sensor position; it is not an individually localized brain region.
- The shaded bands describe trial variability within this participant. No statistical test is performed.

## Repository contents

| File | Purpose |
| --- | --- |
| [tks_kaneshiro2015_erp.ipynb](tks_kaneshiro2015_erp.ipynb) | Clean, runnable notebook |
| [tks_kaneshiro2015_erp_executed.ipynb](tks_kaneshiro2015_erp_executed.ipynb) | Notebook with plots and results from the verified run |
| [FINDINGS.md](FINDINGS.md) | Concise results and interpretation |

## Source

Kaneshiro, B., Perreau Guimaraes, M., Kim, H.-S., Norcia, A. M., & Suppes, P. (2015). *A Representational Similarity Analysis of the Dynamics of Object Processing Using Single-Trial EEG Classification*. PLOS ONE, 10(8), e0135697. [https://doi.org/10.1371/journal.pone.0135697](https://doi.org/10.1371/journal.pone.0135697).
