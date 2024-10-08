# Heterogeneous Graphical Neural Network for Drug Recommendations

This repository contains the implementation of a Heterogeneous Graphical Neural Network (HGNN) for enhancing drug recommendations using Electronic Health Records (EHR). This project, based on our paper "Enhancing Drug Recommendations Via Heterogeneous Graph Representation Learning in EHR Networks," leverages heterogeneous information networks (HINs) to model complex relationships within medical data, improving the accuracy and relevance of medication recommendations.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Models and Methods](#models-and-methods)
- [Datasets](#datasets)
- [Evaluation](#evaluation)
- [Results](#results)


## Overview
Conventional drug recommendation models often fail to capture the complex interactions within EHR data. Our project addresses this limitation by representing EHR data as a Heterogeneous Information Network (HIN) and applying graph representation learning techniques to enhance the drug recommendation process. This approach models various entities (e.g., patients, medications, diagnoses) and their interrelations, allowing for more personalized and accurate drug recommendations.

## Features
- **Heterogeneous Information Network (HIN):** Models EHR data as a HIN to capture multi-entity relationships.
- **Bi-channel Heterogeneous Local Structural Encoder:** Decouples patient-diagnosis and patient-medication interactions for improved analysis.
- **Global Information Capture:** Aggregates meta-paths to represent global data relationships, mitigating information gaps.
- **Handling Cold Start Problem:** Utilizes graph-based methods to recommend drugs for new patients with limited EHR history.

## Installation
To get started, clone the repository and install the necessary dependencies:
git clone https://github.com/harshvardhanrudra/Heterogeneous-Graphical-Neural-Network.git
cd Heterogeneous-Graphical-Neural-Network
pip install -r requirements.txt

## Usage
1. **Preprocess Data:** Prepare the EHR data by generating node and edge representations for the HIN.
2. **Train Model:** Run the training script to train the HGNN model.
3. **Evaluate Model:** Assess model performance on evaluation metrics such as AUC, AP, and Top-K precision.

### Example
python train.py --data_path path/to/dataset --epochs 100 --batch_size 64

## Models and Methods
1. Heterogeneous Graph Representation Learning
   The project employs several advanced techniques to build a robust model, including:

**Bi-channel Local Encoder:** Separates patient-diagnosis and patient-medication interactions.
**Global Information Fusion Module:** Combines meta-paths to create a comprehensive patient representation.
**Recurrent Neural Networks (RNN):** Leverages longitudinal patient information to predict drug recommendations over time.

## Datasets
This project uses public datasets such as MIMIC-III for experimentation. Please ensure to comply with dataset-specific usage rights and licenses.

##Evaluation
Model performance is evaluated using:

**AUC (Area Under Curve):** Measures the model's ability to distinguish between positive and negative drug recommendations.
**AP (Average Precision):** Balances precision and recall.
**Top-K Accuracy:** Evaluates the percentage of correctly recommended drugs among the top-K predictions.

## Results
Our model shows significant improvements in drug recommendation accuracy compared to baseline models, especially for complex cases and patients with multimorbidity. Detailed results and comparisons are available in the results directory.
