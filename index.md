---
title: From Sound to Syllables
subtitle: Measuring birdsong behaviour from raw recordings
---

+++ {"part": "abstract"}
Behaviour starts as raw data: video frames, pose coordinates, or, for a songbird, a pressure wave recorded by a microphone. This short tutorial walks through the first step of any computational behaviour pipeline: turning a raw recording into discrete, measurable units. We take one minute of song from a juvenile zebra finch, compute a spectrogram, detect syllables automatically, check our detector against hand-curated labels, and describe each syllable with a few acoustic features.
+++

## Why birdsong?

Zebra finches learn their song from a tutor, practise it for weeks, and end up singing a stereotyped sequence of syllables called a *motif*. This makes song one of the best-studied learned behaviours in neuroscience: it is easy to record, has clear units, and changes measurably during learning. The same steps you use here (segmentation, feature extraction and comparison with ground truth) apply to pose tracking, vocalisations of other species, and multi-agent recordings.

## Learning objectives

By the end of the tutorial you will be able to:

1. Load an audio recording and visualise it as a waveform and a spectrogram.
2. Explain the time and frequency trade-off when choosing a spectrogram window.
3. Build a simple amplitude-threshold syllable detector.
4. Evaluate a detector against human labels with precision, recall and the F1 score.
5. Describe syllables with duration, pitch-like and noisiness features.

## Prerequisites

:::{list-table}
:header-rows: 1

* - Topic
  - What you need
* - Python
  - NumPy arrays, functions, `for` loops
* - Plotting
  - Basic Matplotlib
* - Maths
  - What a Fourier transform does, at an intuitive level
:::

:::{tip} How to use this book
Each section has a short explanation, a coding exercise and a hidden solution. Try the exercise first, then open the solution to compare. The whole tutorial takes about 60 to 90 minutes.
:::

## Data

We use the *Juvenile Zebra Finch Song Data* from the Mooney lab at Duke University [@qi2026juvenile], released under a CC BY 4.0 licence. The recording is downloaded automatically the first time you run the notebook.
