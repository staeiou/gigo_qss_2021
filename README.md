# Data and code for "'Garbage In, Garbage Out'" Revisited

Click the link below to launch these Jupyter Notebooks in the cloud, where you can run and edit them in your browser, with nothing to install. Click the button, wait for the image to load, then you are in a Jupyter interface. Open the `code` folder to launch the two analysis notebooks. Click the menu "Kernel" -> "Restart and clear output" then the "Run" button to step through each cell yourself. Or click the menu "Kernel" -> "Restart and run all" to re-run the entire notebook.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/staeiou/gigo_qss_2021/HEAD)

## Data overview
All datasets are in `\data\`. The main dataset to explore results is `data\final_labels_hashed_with_scores.xlsx\tsv`. A data dictionary to provide more information about each of the fields in this file is at `data\readme.md`.

- `data\all_labels_hashed.xlsx`: labels for all items by all labelers. Each question is a sheet in the file. Items are rows, columns are labelers, values are labels. 
- `data\all_labels_with_irr_hashed.xlsx`: labels for all items by all labelers, with per-row custom IRR metrics. Same format as `data\all_labels_hashed.xlsx`.
- `data\final_labels_hashed.xlsx`: final labels and metadata, which are analyzed for results. Items are rows, columns are questions.
- `data\final_labels_hashed_with_scores.xlsx\tsv`: final labels and metata, with per-row information scores and other calculated fields. Same format as `data\final_labels_hashed.xlsx`.

## Analysis code overview

All analysis codes are in `\code\` and in Jupyter notebooks with Python 3.7. Specific version numbers of libraries used are in `requirements.txt`. 

- `\code\1-calculate-inter-rater-reliability.ipynb` analyzes `all_labels_hashed.xlsx` to calculate IRR metrics. It outputs `all_labels_with_irr_hashed.xlsx`, which contains per-row values for our custom IRR metrics.

- `\code\2-main-cleaning-analysis-viz.ipynb` analyzes `data\final_labels_hashed.xlsx` to perform all analyses and visualizations. It outputs `data\final_labels_hashed_with_scores.xlsx\tsv`, which contains per-row information scores and other calculated fields. 
