# Bracket Norm Identifies Causally Important Brain Regions From Population Geometry

> All 19 geometric metrics we test predict optogenetic silencing importance only because they track the number of recorded neurons. After controlling for recording yield, all 19 collapse. We propose *bracket norm*, which captures how much a region's choice encoding changes direction as sensory evidence varies. The corrected quantity BN/sqrt(n) is invariant to population size (CV 2.0% across a 25x range), and the top-3 and bottom-3 regions by bracket norm match those by silencing (p = 0.0006). Photoinhibition of ALM *increases* bracket norm by 68% while reducing accuracy, dissociating coding gain from coding direction. On human ECoG, BN/sqrt(n) ranks articulatory motor cortex highest with zero electrode-count confound.

Code and pre-computed results for Tower (2026).

## Setup

```bash
pip install -r requirements.txt
```

## What's here

- `paper/` -- paper source (tex, bib, pdf)
- `figures/` -- scripts that generate Figures 1-3
- `experiments/` -- scripts that produce each table (see [REPRODUCE.md](REPRODUCE.md) for the full mapping)
- `results/` -- pre-computed JSONs so you can verify numbers without re-running
- `data/` -- loaders that auto-download from DANDI/OSF
- `geometry/` -- subspace extraction and distance utilities
- `tests/` -- unit tests (`pytest tests/`)

Most experiment scripts run on CPU from cached Steinmetz data. Cross-dataset validation (IBL, ECoG, Svoboda) used Modal for GPU; those results are included pre-computed.

## Datasets

All publicly available: Steinmetz Neuropixels (DANDI:000028), IBL Brain-Wide Map, Allen Visual Behavior Neuropixels, Svoboda ALM photoinhibition (DANDI:000007/000009), human ECoG (DANDI:000019).

## License

MIT
