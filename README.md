# Uncertainty-Estimation-in-MRI-based-Autism-Spectrum-Disorder-Classification

Graph-based deep learning pipeline for classifying Autism Spectrum Disorder from ABIDE data
#  Project Structure
├── abide_prep.ipynb                 # Prepares ABIDE data (sMRI, fMRI, non-imaging) and saves processed files
├── exploritary_analysis_ABI.ipynb   # Basic exploritary analysis of the data 
├── ev_gcn_main.ipynb                 # Trains the EV-GCN model and evaluates  uncertainty


This project implements a graph-based deep learning pipeline (EV-GCN) for Autism Spectrum Disorder (ASD) classification using the ABIDE neuroimaging dataset. It integrates **advanced uncertainty estimation** methods including:

- Deep Ensemble
- Bayesian Neural Network (BNN)
- Temperature Scaling
- Evidential Deep Learning
- Feature Space Distance
- Gradient-based Uncertainty
- Prediction Interval Estimation

The model outputs interpretable uncertainty metrics, aiding **clinical decision support** by flagging high-uncertainty predictions for expert review.

## Key Features
- Multi-modal input from sMRI + fMRI features
- Population graph construction
- Graph Convolutional Network (GCN) with early stopping
- ECE & AUC-based calibration and performance evaluation
- Comprehensive uncertainty visualizations and rankings

##  How to Run
The project was made on google colab so download and updoad the files to colab then 
1. Download and Prepare the Dataset
Run the notebook abide_prep.ipynb first to:
Download raw ABIDE data (sMRI/fMRI + phenotypic data)
Extract neuroimaging features and harmonize them
Encode categorical metadata (e.g., site, sex, age)
Build graph edges (based on feature similarity or population attributes)
Save preprocessed data into .pkl files for each fold

2. Train EV-GCN and Evaluate Uncertainty 
run the ev_gcn_main.ipynb file 
