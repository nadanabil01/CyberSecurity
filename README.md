# Cyberattack-Detection

## Method description
The aim of the project is to find a mechanism that can detect cyber attacks by analysing flows in a network. To do this, a benchmark of different machine learning methods is performed on a large netflow dataset (see Report).

### Dependencies
- Python 3.6.8
- Numpy 1.16.2
- Pandas 0.24.2
- Scipy 1.2.1
- Datetime 4.3
- h5py 2.9.0
- Matplotlib 3.1.1
- Scikit-learn 0.20.3
- Tensorflow 1.14 -- `predict_neural_network_stat_analysis.py`

### File description
1. `preprocessing1.py` and `preprocessing2.py` are the files used to extract meaningful data from the raw netflow files.

2. `feature_extraction.py` and `pca_tsne.py` try to decrease the number of features using embedded methods or dimensionality reduction techniques.

3. `predict_random_forest_bootstrap.py` and `predict_svm.py` implement a classifier to detect malware with Random Forest and with Support Vector Machine.

4. `predict_gradient_boosting_stat_analysis.py`, `predict_logistic_reg_stat_analysis.py`, `predict_neural_network_stat_analysis.py` and `predict_statistic_analysis_bootstrap.py` carry out statistical analysis of different classifiers: Gradient Boosting, Logistic Regression, Neural Network and Random Forest with bootstrap respectively.

## Results
The experiments show that Random Forest can detect more than 95% of botnets for 8 out of 13 scenarios. Moreover, the accuracy on the 5 most difficult scenarios can be increased thanks to a bootstrap method. For more details, see the report.
