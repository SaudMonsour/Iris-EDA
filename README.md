# Understanding iris species measurements

**2026-09-05 · EDA · Automatically executed · Human review pending**

## Research question

How do flower measurements vary across species, and which measurements are associated?

## Results

The exploratory dataset contains 149 usable rows and 4 candidate features.

The strongest absolute Pearson feature correlation in the exploratory sample was petal length (cm) / petal width (cm) (|r| = 0.963); this suggests checking redundancy, not concluding causality.

## Analysis scope

This is an exploratory study. No predictive performance score is reported. A descriptive question was selected.

## Data provenance

Source: [https://archive.ics.uci.edu/dataset/53/iris](https://archive.ics.uci.edu/dataset/53/iris)

License: CC BY 4.0. Attribution and source description are in SOURCE.md. The exact analyzed snapshot and its SHA-256 are retained.

## Data quality

| Check | Value |
| --- | --- |
| original rows | 150 |
| original features | 4 |
| missing cells | 0 |
| missing target rows removed | 0 |
| exact duplicates removed | 1 |
| usable rows | 149 |

Excluded from predictors: none specified. See data_dictionary.csv for column types, missingness and uniqueness.

## Visual evidence

![Missing values and target distribution](figures/data-quality.png)

Missing values and target distribution.

![Numeric feature distributions; up to six features by training/sample variance](figures/distributions.png)

Numeric feature distributions; up to six features by training/sample variance.

![Feature associations; correlation does not imply causation](figures/correlations.png)

Feature associations; correlation does not imply causation.

## Limitations

This is a tiny, curated benchmark. Correlations and visible class separation do not establish causal relationships.

The automated pipeline cannot infer all leakage paths, sampling bias, entity grouping or business meaning. Feature importance is post-hoc and is not used to choose the winner. Any follow-up tuned after inspecting this holdout needs a fresh final evaluation.

## Reproduce

From the repository root, install requirements.txt and run:

```bash
python daily_ds/reproduce.py projects/2026-09-05-iris
```

The command uses the saved snapshot, configuration and dataset specification, and writes to reproduced/. analysis.ipynb provides a readable walkthrough. Numeric results may differ slightly across platforms; software versions and code hashes are recorded.

## Your contribution

This study was generated and executed by an automated agent. It has not been reviewed by Saud. Use LEARNING_NOTES.md to record your own explanation, changed code, new experiment and measured outcome; leave unanswered fields blank.
