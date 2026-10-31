# TKS Replicate mini-project — concise findings

## What was run

- **Dataset:** Kaneshiro2015 through MOABB; participant 1 only.
- **Conditions:** human face, animal face, and inanimate object.
- **Small-sample rule:** the first 60 stimulus-locked trials from each condition (180 trials total).
- **Signal summary:** mean across the 20 most posterior HydroCel sensors, then across trials; sampling is 62.5 Hz and epochs span 0–496 ms after stimulus onset.
- **No classifier or ML:** this is an ERP visualization and descriptive summary only.

## Observed descriptive result

| Condition | Trials | Mean amplitude, 200–350 ms (µV) | Largest absolute mean | Time |
| --- | ---: | ---: | ---: | ---: |
| Human face | 60 | +0.025 | +0.127 µV | 224 ms |
| Animal face | 60 | +0.017 | +0.118 µV | 224 ms |
| Inanimate object | 60 | −0.006 | +0.097 µV | 224 ms |

All three posterior averages showed a positive deflection centered near 224 ms. In this fixed, one-participant sample, the human-face trace was numerically largest and the inanimate-object trace smallest in the 200–350 ms window. The uncertainty bands in the notebook are trial-wise SEM bands, not inferential confidence intervals.

## Limits on the conclusion

This does **not** establish category selectivity or reproduce the original paper’s classification/RSA results. The comparison is limited to one participant, a chronological 60-trial cap per condition, a position-defined sensor ROI, and data that begin at stimulus onset with no prestimulus baseline. No hypothesis test or multiple-participant analysis was run.

## Sources

- Kaneshiro, B., Perreau Guimaraes, M., Kim, H.-S., Norcia, A. M., & Suppes, P. (2015). *A Representational Similarity Analysis of the Dynamics of Object Processing Using Single-Trial EEG Classification*. PLOS ONE, 10(8), e0135697. https://doi.org/10.1371/journal.pone.0135697
- MOABB, [Kaneshiro2015 dataset documentation](https://moabb.neurotechx.com/docs/generated/moabb.datasets.Kaneshiro2015.html).
