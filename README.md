# Skeleton-Based Action Recognition Code

This folder contains the Jupyter notebooks used for the project experiments:

- `mlp_skeleton_baseline_colab.ipynb`
- `lstm_skeleton_baseline_colab.ipynb`
- `CNN_skeleton.ipynb`
- `stgcn_skeleton.ipynb`

## Environment

The notebooks were designed to run on Google Colab with a GPU runtime.

Required packages:

- `torch`
- `numpy`
- `matplotlib`
- `scikit-learn`
- `pandas`

These packages are usually available by default in Colab.

## Dataset

The experiments use the HRNet NTU RGB+D 60 2D skeleton dataset file:

```text
ntu60_hrnet.pkl
```

Dataset source page:

```text
https://github.com/kennymckormick/pyskl/blob/main/tools/data/README.md
```

On that page, click:

```text
NTURGB+D [2D Skeleton]
```

Direct download link:

```text
https://download.openmmlab.com/mmaction/pyskl/data/nturgbd/ntu60_hrnet.pkl
```

Place the file in Google Drive at:

```text
/content/drive/MyDrive/ntu60_hrnet.pkl
```

Each notebook loads the dataset from this path. If the file is stored elsewhere, update `PKL_PATH` near the beginning of the notebook.

## How To Run

1. Open a notebook in Google Colab.
2. Select `Runtime -> Change runtime type -> GPU`.
3. Run all cells from top to bottom.
4. Repeat for each model notebook.

The notebooks train the model, save the best checkpoint, plot training curves, generate confusion matrices, and export classification reports.

## Outputs

By default, results are written to:

```text
/content/drive/MyDrive/skeleton_project_outputs/
```

Expected output subfolders:

- `mlp`
- `lstm`
- `cnn`
- `stgcn`

Each output folder contains the best model checkpoint, training history CSV, training curve figure, confusion matrices, top-confusion CSV files, and classification report.

## Report Reproduction

The final report uses the exported results from `skeleton_project_outputs`. The reported final validation accuracies are:

- MLP: 49.51%
- LSTM: 70.66%
- CNN: 75.10%
- ST-GCN: 82.22%
