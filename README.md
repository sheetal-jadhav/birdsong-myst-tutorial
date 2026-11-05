# From Sound to Syllables

A short, interactive tutorial on measuring birdsong behaviour, built with [JupyterBook 2](https://jupyterbook.org) and [MyST](https://mystmd.org).

Using one minute of juvenile zebra finch song, the tutorial covers:

1. Spectrograms and the time-frequency trade-off
2. Amplitude-threshold syllable detection
3. Evaluation against hand labels (intersection over union)
4. Acoustic features (peak frequency, Wiener entropy, duration) and a precision/recall trade-off
5. Song rhythm from inter-onset intervals

Each section has a coding exercise with a hidden solution, written in the style of Neuromatch Academy tutorials.

## Run locally

```bash
pip install -r requirements.txt
jupyter book start --execute      # live preview at http://localhost:3000
```

Or open `tutorials/birdsong_segmentation.ipynb` in Jupyter or Google Colab. The audio downloads automatically from Zenodo on first run.

## Deployment

Every push to `main` triggers `.github/workflows/deploy.yml`, which executes the notebook, fails the build on any error (`--strict`), and publishes the site to GitHub Pages.

## Data

Qi, J. & Mooney, R. (2026). *Juvenile Zebra Finch Song Data* (v1). Zenodo. https://doi.org/10.5281/zenodo.20411580, licensed CC BY 4.0.

## License

Text and figures: CC BY 4.0. Code: BSD 3-Clause.
