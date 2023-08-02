# Hypertension Detection From High-Dimensional Representation of Photoplethysmogram Signals

The paper has been accepted at IEEE-EMBS International Conference on Biomedical and Health Informatics (BHI’23), Oct. 15–18, 2023, Pittsburgh, Pennsylvania, USA.

This repository contains the codes corresponding to study hypertension detection from PPG using MiniROCKET.

## Requirements
Please install the following Python (3.8) libraries:

- pyampd
- scipy
- mat73
- sklearn
- pandas
- numpy
- matplotlib
- seaborn
- h5py
- imblearn

## Usage 
 1- Download the dataset (~32 GB) from
 https://zenodo.org/record/5590603/files/MIMIC-III_ppg_dataset.h5?download=1
 
 2- Convert the downloaded h5 file to tfrecords using the script available on:
 https://github.com/Fabian-Sc85/non-invasive-bp-estimation-using-deep-learning/tree/main#creating-tfrecord-datasets-for-training
 
 3- Follow and run Hypertension_PPG_MiniROCKET.ipynb for the next steps.
 

## Results

### Performance

The results demonstrate the feasibility of hypertension detection from PPG using random convolution kernels on completely unseen subjects, with a weighted average F1-score of 71.6% and sensitivity of 69.1%. 

Relying solely on the heart-rate feature for hypertension detection leads to a significantly lower sensitivity of 50.3%. Although this sensitivity is slightly better than chance level, it alone is insufficient for detecting hypertension. This indicates that in addition to heart rate, PPG can provide many BP-related informative attributes that can enhance classification performance significantly.

### Impact of the Number of Training Samples

In order to study the effect of training set size on the models' performance, the models were trained using varying percentages of the training samples: 6.25%, 12.5%, 25%, and 50%. The figure below illustrates the performance of different models as the size of the training set increases.

When only 50% of the training data was used, the highest F1-score amongst the models dropped from 71.6% to 69.2%. Similarly, using 25% of the training samples led to a further decrease to 65.0%. In all scenarios, MiniROCKET consistently outperformed all other methods. The trends indicated by this plot suggest that increasing the size of the training dataset, can result in higher classification accuracy.

![dataset_size_hypertension_performance](plots/dataset_size_hypertension_performance.png)

## Citing this work
Please use the following citation:
```
Hasanzadeh, N., Valaee, S. and Salehinejad, H., 2023. Hypertension Detection From High-Dimensional Representation of Photoplethysmogram Signals. arXiv: []
```
