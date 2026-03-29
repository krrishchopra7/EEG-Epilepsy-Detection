# EEG Epilepsy Detection

This repository contains my work on epileptic seizure detection from EEG signals using both classical machine learning models and a graph-based deep learning approach.

The goal of the project is to compare how different modeling strategies behave on EEG classification tasks, including 2-class, 3-class, and 5-class setups. I used notebooks so the full pipeline stays easy to follow, from loading data and preprocessing to training, evaluation, and visualizing results.

## What's in the repo

- `Epilepsy_SVM,RF,MLP,XgBoost.ipynb`
  A notebook that experiments with multiple baseline models including SVM, Random Forest, XGBoost, and MLP. It covers preprocessing, training, evaluation metrics, confusion matrices, and summary comparisons across different classification settings.

- `Epilepsy_GAT.ipynb`
  A graph attention network based approach for EEG epilepsy detection. This notebook explores a deeper learning setup where EEG samples are handled in a graph-style modeling pipeline instead of only standard tabular ML methods.

## Project workflow

The notebooks follow a practical end-to-end workflow:

1. Load EEG data and organize labels.
2. Prepare features for binary, 3-class, and 5-class experiments.
3. Train multiple models.
4. Evaluate with accuracy, precision, recall, F1-score, and confusion matrices.
5. Compare results across experiments to understand which approach is more reliable.

## Current result snapshot

From the baseline notebook, the reported accuracies are:

| Experiment | SVM | Random Forest | XGBoost | MLP |
| --- | ---: | ---: | ---: | ---: |
| 2-Class | 0.96 | 0.94 | 0.92 | 0.93 |
| 3-Class | 0.92 | 0.86 | 0.84 | 0.87 |
| 5-Class | 0.69 | 0.58 | 0.58 | 0.60 |

These results suggest that the simpler classification settings are much easier to separate, while the full 5-class problem is noticeably more challenging.

## Why I built this

I wanted to explore epilepsy detection from more than one angle instead of stopping at a single model. The classical models give a strong baseline and are easier to interpret, while the GAT notebook lets me test whether graph-based deep learning can capture richer structure in EEG data.

## Running the notebooks

To work with this project locally:

1. Clone the repository.
2. Open the notebooks in Jupyter Notebook, JupyterLab, or Google Colab.
3. Install the Python libraries used in the notebooks if they are not already available in your environment.
4. Update dataset paths inside the notebooks if needed before running all cells.

## Notes

- The notebooks currently serve as the main source of code and experimentation.
- Dataset files are not included here, so you may need to point the notebooks to your own EEG dataset location.
- Some outputs in the notebooks are saved for reference so the experiment flow is easier to review.

## Future improvements

- Move reusable code into Python scripts or modules.
- Add a `requirements.txt` file for easier setup.
- Document the dataset source and folder structure more clearly.
- Add a dedicated results section with saved figures and model comparisons.

## Author

Krrish Chopra
