# Data and code for "'Garbage In, Garbage Out'" Revisited

Note: this paper is in peer review (but not a mutually-anonymous / double-blind process). This repository is currently intended for the peer reviewers. We have not yet released a preprint of our draft. However, contact Stuart Geiger if you would like to review a preprint privately.

# Inventory
- `\data\`: first-round labels, final labels, metadata, and scores for each paper
- `\code\`: all data cleaning and analyses for every statistic and graph
- `\figures\`: all graphs and figures, in png, pdf, and eps formats
- `appendix.pdf`: supplementary findings and instructions/definitions given to labelers

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

## Explore with mybinder.org

Click the link below to launch these Jupyter Notebooks in the cloud, where you can run and edit them in your browser, with nothing to install. Click the button, wait for the image to load, then you are in a Jupyter interface. Open the `code` folder, then click on one of the two analysis notebooks to launch. When in the notebook, click the "Run" button in the center of the toolbar to step through each code and documentation cell yourself. Or click the menu "Kernel" -> "Restart and run all" to re-run the entire notebook.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/staeiou/gigo_qss_2021/HEAD)


[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4906637.svg)](https://doi.org/10.5281/zenodo.4906637)

