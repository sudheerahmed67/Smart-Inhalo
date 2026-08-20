# Smart-Inhalo
AI-based respiratory technique analysis using machine learning and deep learning

## 📌 Overview

Smart-Inhalo is an AI-assisted respiratory analysis project designed as the
foundation for a smart inhaler system. The project analyzes respiratory
breathing-cycle features such as airflow, pressure, tidal volume, and chest
and abdominal movement to classify breathing technique as Correct or Wrong.

The current system is a research prototype and uses technical/proxy labels.
These labels are not clinically validated inhaler-technique labels.

## 🎯 Objectives

- Analyze respiratory breathing patterns
- Extract meaningful respiratory features
- Identify technically abnormal breathing patterns
- Compare classical machine-learning models
- Develop a deep-learning baseline
- Prepare the model for future Smart-Inhalo deployment

## 📊 Dataset

The main respiratory data was obtained from the PhysioNet Respiratory Dataset.

The processed dataset contains:

- 79 subjects with usable breathing cycles
- 13,137 clean breathing cycles
- Respiratory cycle-level features
- Flow measurements
- Pressure measurements
- Tidal-volume measurements
- Chest movement
- Abdominal movement

The original public dataset is processed into a project-specific dataset
through cycle extraction, quality control, feature engineering, and technical
label generation.

## 🔧 Data Processing

The project follows this pipeline:

Raw Respiratory Data
→ Quality Control
→ Breathing Cycle Extraction
→ Feature Engineering
→ Technical Labels
→ Subject-Level Train/Test Split
→ Feature Scaling
→ ML/DL Training
→ Evaluation

## 🧪 Features

Important respiratory features include:

- Cycle Duration
- Peak Flow
- Minimum Flow
- Mean Flow
- Flow Range
- Flow Variability
- Peak Pressure
- Minimum Pressure
- Mean Pressure
- Pressure Range
- Pressure Variability
- Tidal Volume
- Chest Movement
- Abdominal Movement

Additional derived features include:

- Flow/Pressure Ratio
- Volume/Duration Ratio
- Flow Variability
- Pressure Variability

## 🏷️ Labeling

The project uses technical/proxy labels based on respiratory feature
deviations.

The labels are:

- Correct
- Wrong

These labels are intended for technical model development and should not be
interpreted as clinically validated inhaler-technique diagnoses.

## 🤖 Machine Learning Models

The project compares:

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)

## 🧠 Deep Learning

A feed-forward neural network (MLP) is also developed using the processed
respiratory features.

The deep-learning pipeline includes:

- Feature scaling
- Dense layers
- ReLU activation
- Batch normalization
- Dropout
- Adam optimizer
- Binary classification

## 📈 Evaluation

Models are evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- Confusion Matrix
- ROC-AUC
- Precision-Recall analysis

A subject-level split is used so that breathing cycles from the same subject
do not appear in both training and testing datasets.

## ⚠️ Limitations

- Current labels are technical/proxy labels rather than clinically validated
  inhaler-technique labels.
- The current dataset contains cycle-level features rather than raw inhaler
  sensor waveforms.
- Public respiratory recordings are not equivalent to controlled inhaler-use
  recordings.
- Further real-world data collection is required.
- Clinical validation is required before making medical claims.

## 🚀 Future Work

Future development will focus on:

- Collecting real Smart-Inhalo sensor data
- Integrating airflow and pressure sensors
- Adding inhaler orientation detection
- Using raw time-series respiratory signals
- Exploring CNN/LSTM/Transformer architectures
- Real-time inference on embedded hardware
- ESP32 integration
- Real-time user feedback
- Clinical validation

## 📁 Project Structure

```text
Smart-Inhalo/
│
├── notebooks/
│   └── Smart_Inhalo_Hybrid_ML_DL.ipynb
│
├── models/
│   └── trained_models
│
├── data/
│   └── README.md
│
├── requirements.txt
└── README.md
