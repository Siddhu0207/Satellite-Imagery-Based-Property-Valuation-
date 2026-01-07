# Satellite-Imagery-Based-Property-Valuation-
A hybrid regression model combining satellite imagery and tabular data for property valuation
#  Multimodal Real Estate Valuation Pipeline

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Completed-success)
![Library](https://img.shields.io/badge/Library-XGBoost%20%7C%20Pandas%20%7C%20Mapbox-orange)

A hybrid Machine Learning pipeline that predicts property prices by fusing **structured housing data** (financial specs) with **satellite imagery** (environmental context). This project integrates visual "curb appeal" features (greenery, density, road proximity) into a robust XGBoost pricing model.

##  Repository Contents

| File | Type | Description |
| :--- | :--- | :--- |
| **`data_fetcher.py`** |Script | **Data Acquisition.** Automated tool to download satellite imagery (600x600) from Mapbox API for every property. Features parallel processing and retry logic. |
| **`preprocessing.ipynb`** | Notebook | **EDA & Geospatial Analysis.** Visualizes price distributions on interactive maps, cleans raw data, and analyzes location correlations. |
| **`model_training.ipynb`** |  Notebook | **Modeling Engine.** The core pipeline. Performs feature extraction, trains the hybrid XGBoost/Ensemble model, and validates performance. |
| **`23115101_report.pdf`** |Report | **Project Documentation.** A comprehensive report detailing the methodology, architecture diagrams, visual insights (Grad-CAM), and financial results. |
| **`23115101_final.csv`** |Data | **Final Deliverable.** The predicted price outputs for the test dataset. |

---

## Key Features
* **Multimodal Learning:** Integrates numerical data (sqft, bedrooms) with visual data (satellite view).
* **Automated Data Ingestion:** Uses `ThreadPoolExecutor` to handle thousands of API requests efficiently.
* **Robust Modeling:** Implements a "Grandmaster Hybrid" approach using XGBoost, PCA (Principal Component Analysis), and Clustering features.

---

## Setup & Installation

### 1. Prerequisites
Ensure you have Python 3.8+ installed. Install the required dependencies:

```bash
pip install pandas numpy xgboost scikit-learn plotly matplotlib seaborn requests openpyxl tqdm
