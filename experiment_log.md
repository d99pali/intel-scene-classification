| Experiment | Val Accuracy | Val Loss | Train Accuracy | Train Loss | Notes |
|---|---|---|---|---|---|
| Baseline CNN (v1) | 0.7578 | 2.0960 | 0.9971 | 0.0160 | Overfitting — val_loss diverges ~epoch 5 |
| Dropout 0.35 (was 0.2) | 0.7156 | 2.2356 | 0.9948 | 0.0201 | No meaningful improvement — train accuracy barely changed (99.5% vs 99.7%), suggesting a single dropout layer after Dense(128) isn't sufficient to constrain memorization. Moving to Batch Normalization next rather than pushing dropout further.
