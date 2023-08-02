# Hypertension Detection From High-Dimensional Representation of Photoplethysmogram Signals

Accepted at IEEE-EMBS International Conference on Biomedical and Health Informatics (BHI’23)

This repository contains the codes corresponding to study hypertension using PPG.

## Requirements
Please install the following Python (3.8) libraries:

- pyampd
- scipy
- mat73
- sklearn
- pandas
- numpy
- matplotlib
- pickle
- h5py
- imblearn

## Usage 
 1- Download the dataset (~32 GB) from
 https://zenodo.org/record/5590603/files/MIMIC-III_ppg_dataset.h5?download=1
 
 2- Convert the downloaded h5 file to tfrecords using the script available on:
 https://github.com/Fabian-Sc85/non-invasive-bp-estimation-using-deep-learning/tree/main#creating-tfrecord-datasets-for-training
 
 3- Follow and run Hypertension_PPG_MiniROCKET.ipynb for the next steps.
 

## Results
The results show the feasibilty of hypertension detection from PPG using random covoultion kernels  on completely unseen subjects with weighted average F1-score of 71.6% and sensetivity of 69.1%.

![RegPlot_sys_RandomForest](plots/dataset_size_hypertension_performance.png)

## Citing this work
Please use the following citation:
```
Hasanzadeh, N., Valaee, S. and Salehinejad, H., 2023. Hypertension Detection From High-Dimensional Representation of Photoplethysmogram Signals. arXiv: []
```
