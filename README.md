# Afghanistan Aid Targeting Replication Repo

This repo contains the replication code for the paper "Program targeting with machine learning and mobile phone data: Evidence from an anti-poverty intervention in Afghanistan" by Emily Aiken, Guadalupe Bedoya, Joshua Blumenstock, and Aidan Coville (2022). The repo is structured as follows:

### Data
- `data/survey.csv`: Synthetic household survey data
- `data/phone_features.csv`: Synthetic featurized phone data, containing around a thousand features relating to mobile phone use 
- `data/interim_analysis_datasets`: Most datasets saved during the analysis will be stored here

### Scripts
- `data/generate_synthetic_data.ipynb`: Generates the synthetic survey and phone features datasets; adjust parameters for more or fewer observations, or to inject correlations between variables
- `0requirements.ipynb`: Installs the required packages for the subsequent replication scripts 1-4
- `1survey.ipynb`: Analysis of raw survey data and generation of additional survey-based outcomes (asset index, below poverty line)
- `2machinelearning.ipynb`: Implementation and evaluation of machine learning models to predict survey outcomes from mobile phone features
- `3targeting.iynb`: Targeting simulations to compare accuracy of targeting methods
- `4costs.ipynb`: Calculation of targeting costs for PMT, CBT, and the phone-based approach

### Results
- `results/tables`: All tables that are present in the paper are saved here in .csv format
- `results/figures`: All figures that are present in the paper are saved here in .png format
- `results/simulations`: Results from machine learning models (predictions, feature importances, the models themselves) are saved here

### Dependencies
- python = 3.7.7
- numpy = 1.18.5
- pandas = 1.0.5
- matplotlib = 3.3.2
- seaborn = 0.10.1
- scikit-learn = 0.23.1
- scikit-misc = 0.1.3
- lightgbm = 2.3.0
- joblib = 0.15.1
