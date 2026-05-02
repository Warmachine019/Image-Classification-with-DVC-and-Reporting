# Reproducible Image Classification Pipeline
## Overview
This project is an automated Machine Learning pipeline built within the Jupyter Ecosystem (Google Colab). It trains a Convolutional Neural Network (CNN) to classify images using the CIFAR-10 dataset.
Rather than just focusing on AI accuracy, this project demonstrates real-world Software Engineering for AI (SEAI) best practices: making sure the code is perfectly repeatable, the data is safely backed up, and the final results are automatically documented.

## Core Features
Reproducibility: Enforces strict random seeding across PyTorch, NumPy, and Python's random modules to guarantee the exact same training results every time the pipeline is run.
Data Versioning: Integrates DVC (Data Version Control) to track datasets exactly like Git tracks code, using Google Drive as the backend storage.
Automated Reporting: Uses nbconvert to automatically compile the notebook, output logs, and JSON metrics into a clean, static HTML report for stakeholders.

## Tech Stack
Environment: Google Colab / Jupyter Notebooks
Deep Learning: PyTorch (torch, torchvision)
MLOps Tools: DVC (Data Version Control)
Reporting: nbconvert, json
Dataset: CIFAR-10 (32x32 pixel images across 10 classes)

## How to Run in Google Colab
Because this project utilizes DVC and automated HTML exports, it requires a persistent file system. We use Google Drive for this.
Upload the .ipynb notebook file to your Google Drive.
Open the notebook using Google Colab.
Run the first cell to mount your Google Drive.
Run the notebook from top to bottom. The pipeline will automatically:
Initialize a DVC repository in your Drive.
Download and version the CIFAR-10 dataset.
Train the SimpleCNN model.
Save the final metrics to a metrics.json file.
Generate a full report.html file in your project folder.
