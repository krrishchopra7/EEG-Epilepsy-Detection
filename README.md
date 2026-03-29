# EEG Epilepsy Detection

This repository contains our work on epileptic seizure detection from EEG signals using both classical machine learning models and a graph-based deep learning approach.

The goal of the project is to compare how different modeling strategies behave on EEG classification tasks, including 2-class, 3-class, and 5-class setups. We used notebooks so the full pipeline stays easy to follow, from loading data and preprocessing to training, evaluation, and visualizing results.

## What's in the repo

- `Epilepsy_SVM,RF,MLP,XgBoost.ipynb`
  A notebook that experiments with multiple baseline models including SVM, Random Forest, XGBoost, and MLP. It covers preprocessing, training, evaluation metrics, confusion matrices, and summary comparisons across different classification settings.

- `Epilepsy_GAT.ipynb`
  Our proposed model. This notebook implements a Graph Attention Network (GAT) based approach for EEG epilepsy detection and explores how graph-based deep learning can capture relationships in EEG data beyond standard tabular baselines.

## Project workflow

The notebooks follow a practical end-to-end workflow:

1. Load EEG data and organize labels.
2. Prepare features for binary, 3-class, and 5-class experiments.
3. Train multiple models.
4. Evaluate with accuracy, precision, recall, F1-score, and confusion matrices.
5. Compare results across experiments to understand which approach is more reliable.

## Current result snapshot

The table below gives a single comparison view of the main results from the notebooks. The classical models are reported across 2-class, 3-class, and 5-class experiments, while GAT is included as our proposed model with the metrics saved in its evaluation notebook.

| Model | Experiment | Accuracy | Precision | Recall | F1-score |
| --- | --- | ---: | ---: | ---: | ---: |
| SVM | 2-Class | 0.96 | 0.96 | 0.95 | 0.96 |
| SVM | 3-Class | 0.92 | 0.91 | 0.93 | 0.92 |
| SVM | 5-Class | 0.69 | 0.69 | 0.69 | 0.68 |
| Random Forest | 2-Class | 0.94 | 0.94 | 0.93 | 0.94 |
| Random Forest | 3-Class | 0.86 | 0.86 | 0.83 | 0.84 |
| Random Forest | 5-Class | 0.58 | 0.59 | 0.58 | 0.58 |
| XGBoost | 2-Class | 0.92 | 0.92 | 0.91 | 0.92 |
| XGBoost | 3-Class | 0.84 | 0.86 | 0.80 | 0.82 |
| XGBoost | 5-Class | 0.58 | 0.58 | 0.58 | 0.58 |
| MLP | 2-Class | 0.93 | 0.94 | 0.92 | 0.93 |
| MLP | 3-Class | 0.87 | 0.87 | 0.87 | 0.87 |
| MLP | 5-Class | 0.60 | 0.59 | 0.60 | 0.58 |
| GAT (Proposed) | Notebook evaluation | 0.95 | 0.95 | 0.94 | 0.95 |

These results suggest that the simpler classification settings are much easier to separate, while the full 5-class problem is noticeably more challenging. The proposed GAT model also shows strong performance in its saved evaluation results.

## Why we built this

We wanted to explore epilepsy detection from more than one angle instead of stopping at a single model. The classical models give strong baselines and are easier to interpret, while the GAT notebook lets us test whether graph-based deep learning can capture richer structure in EEG data.

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

## Contributors

- Krrish Chopra
- Sanket
- Ronit
- Navprabhat
