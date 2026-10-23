# Training Log: Student Pass/Fail Neural Network

## Run Summary

| Item | Value |
|---|---|
| Epochs | 50 |
| Batches per epoch | 1 |
| Validation split | 20% of training data (about 3 samples) |
| Optimizer / Loss | Adam / binary cross-entropy |
| Final train accuracy | 0.5833 |
| Final train loss | 0.6401 |
| Final validation accuracy | 0.7500 |
| Final validation loss | 0.5067 |
| Time per step | about 80 to 130 ms |

## Key Observations

- **Loss fell steadily in both sets.** Training loss dropped from 0.7814 to 0.6401. Validation loss dropped from 0.7171 to 0.5067. The model is learning, but it has not converged.
- **Training accuracy stayed low for most of the run.** It sat around 0.33 to 0.42 until epoch 43, then rose to 0.5833 by epoch 46.
- **Validation accuracy is unreliable.** The validation set has only about 3 samples, so each sample shifts accuracy by roughly 0.33. The value moved between 0.50 and 0.75 and never changed by smaller steps.
- **Final prediction step** ran on the 4-row test set. The log shows only the progress bar. The `Accuracy:` line is not in this log.

## Epoch-by-Epoch Metrics

| Epoch | Train Acc | Train Loss | Val Acc | Val Loss |
|---:|---:|---:|---:|---:|
| 1 | 0.3333 | 0.7814 | 0.7500 | 0.7171 |
| 2 | 0.3333 | 0.7777 | 0.7500 | 0.7099 |
| 3 | 0.4167 | 0.7739 | 0.5000 | 0.7029 |
| 4 | 0.4167 | 0.7702 | 0.5000 | 0.6961 |
| 5 | 0.4167 | 0.7666 | 0.5000 | 0.6894 |
| 6 | 0.4167 | 0.7630 | 0.5000 | 0.6829 |
| 7 | 0.4167 | 0.7594 | 0.5000 | 0.6765 |
| 8 | 0.4167 | 0.7559 | 0.5000 | 0.6702 |
| 9 | 0.4167 | 0.7523 | 0.5000 | 0.6641 |
| 10 | 0.4167 | 0.7488 | 0.5000 | 0.6581 |
| 11 | 0.4167 | 0.7453 | 0.5000 | 0.6523 |
| 12 | 0.4167 | 0.7419 | 0.5000 | 0.6466 |
| 13 | 0.4167 | 0.7384 | 0.5000 | 0.6410 |
| 14 | 0.4167 | 0.7350 | 0.5000 | 0.6356 |
| 15 | 0.4167 | 0.7317 | 0.5000 | 0.6303 |
| 16 | 0.4167 | 0.7284 | 0.5000 | 0.6251 |
| 17 | 0.4167 | 0.7252 | 0.5000 | 0.6201 |
| 18 | 0.4167 | 0.7221 | 0.5000 | 0.6151 |
| 19 | 0.4167 | 0.7189 | 0.5000 | 0.6103 |
| 20 | 0.4167 | 0.7159 | 0.5000 | 0.6056 |
| 21 | 0.4167 | 0.7128 | 0.5000 | 0.6011 |
| 22 | 0.4167 | 0.7098 | 0.5000 | 0.5966 |
| 23 | 0.4167 | 0.7068 | 0.5000 | 0.5922 |
| 24 | 0.4167 | 0.7039 | 0.5000 | 0.5879 |
| 25 | 0.4167 | 0.7010 | 0.5000 | 0.5837 |
| 26 | 0.4167 | 0.6981 | 0.5000 | 0.5796 |
| 27 | 0.4167 | 0.6953 | 0.5000 | 0.5756 |
| 28 | 0.4167 | 0.6925 | 0.5000 | 0.5717 |
| 29 | 0.4167 | 0.6898 | 0.5000 | 0.5679 |
| 30 | 0.4167 | 0.6871 | 0.5000 | 0.5642 |
| 31 | 0.4167 | 0.6844 | 0.5000 | 0.5605 |
| 32 | 0.4167 | 0.6818 | 0.5000 | 0.5570 |
| 33 | 0.4167 | 0.6792 | 0.7500 | 0.5535 |
| 34 | 0.4167 | 0.6766 | 0.7500 | 0.5501 |
| 35 | 0.4167 | 0.6740 | 0.7500 | 0.5468 |
| 36 | 0.3333 | 0.6715 | 0.7500 | 0.5435 |
| 37 | 0.3333 | 0.6691 | 0.7500 | 0.5404 |
| 38 | 0.3333 | 0.6667 | 0.7500 | 0.5373 |
| 39 | 0.3333 | 0.6644 | 0.7500 | 0.5343 |
| 40 | 0.3333 | 0.6621 | 0.7500 | 0.5315 |
| 41 | 0.4167 | 0.6598 | 0.7500 | 0.5287 |
| 42 | 0.4167 | 0.6576 | 0.7500 | 0.5260 |
| 43 | 0.4167 | 0.6553 | 0.7500 | 0.5233 |
| 44 | 0.5000 | 0.6531 | 0.7500 | 0.5208 |
| 45 | 0.5000 | 0.6509 | 0.7500 | 0.5183 |
| 46 | 0.5833 | 0.6487 | 0.7500 | 0.5159 |
| 47 | 0.5833 | 0.6465 | 0.7500 | 0.5135 |
| 48 | 0.5833 | 0.6444 | 0.7500 | 0.5112 |
| 49 | 0.5833 | 0.6422 | 0.7500 | 0.5089 |
| 50 | 0.5833 | 0.6401 | 0.7500 | 0.5067 |

## Possible Next Steps

- **Train longer or raise the learning rate.** Loss is still falling at epoch 50, so the model is undertrained.
- **Use more data.** With 20 rows in the original file, validation and test accuracy are too noisy to compare runs. The 200-row synthetic file should give steadier numbers.
- **Report the test accuracy.** The `Accuracy:` line from the script is the figure to record for the final result.
