# Multi-Agent Network Fault Management — Research Code

This repository contains the Jupyter Notebook used for the network fault management experiments.

## Contents

- `notebookedd4e3d884.ipynb` — complete experiment notebook, including:
  - packet-traffic anomaly detection using `Captured_packets.csv`
  - graph-based fault diagnosis experiments
  - recovery-agent experiments
  - safety-shield evaluation
  - integrated closed-loop evaluation
  - environment/version reporting and results export

## Dataset

The detection experiment expects a CSV file named `Captured_packets.csv`.

1. Download the dataset from Kaggle:
   https://www.kaggle.com/datasets/deavanathan/network-traffic-dataset-captured-through-wireshark
2. In Kaggle Notebooks, choose **Add Input** and attach the dataset.
3. Confirm that the attached dataset contains `Captured_packets.csv`.

The notebook searches under `/kaggle/input/` for this exact filename. If your downloaded CSV has a different filename, update the dataset-search cell accordingly.

## How to run

**Recommended environment: Kaggle Notebooks**

1. Create a new Kaggle Notebook.
2. Upload/import this `.ipynb` notebook.
3. Attach the Kaggle dataset using **Add Input**.
4. Enable Internet in Notebook settings if package installation is required and permitted.
5. Run the notebook cells from top to bottom.

The first code cell installs some required packages. The notebook creates experiment files under `/kaggle/working/nfm_experiments/` and saves results under its `results/` directory. The final cell packages the results as `results.zip`.

## Important reproducibility notes

- Run all cells in order; later experiments depend on files created by earlier cells.
- The full recovery experiment and integrated evaluation may take substantial time and compute.
- The diagnosis/recovery simulator is synthetic, as described in the notebook. The detection experiment uses the attached packet CSV.
- Results may vary with software versions, available hardware, and execution environment.
- This repository currently contains the notebook only. Any additional data, model checkpoints, or generated result files must be supplied separately if needed to reproduce a particular run.

## Dataset license

The Kaggle dataset page indicates **MIT License**. Dataset access date should reflect the date the researcher actually accessed/downloaded it.
