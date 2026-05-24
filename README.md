# DOCC URL Classification System

## Overview

The DOCC URL Classification System is a two-stage machine learning pipeline designed for cybersecurity and threat intelligence applications.

The system takes a URL as input and performs:

1. URL Reputation Analysis
2. Website Type Classification

The primary objective is to detect malicious/suspicious URLs and classify trusted websites into meaningful categories.

---

# Architecture

## Stage 1 — Reputation Classification Model

This model predicts whether a URL/domain is benign or suspicious using threat intelligence and reputation-based features.

### Model Details

* Model: Gradient Boosting Classifier
* Accuracy: 98.7%
* Weighted F1-Score: 98.8%

### Training Data Sources

* URLhaus
* Spamhaus
* Tranco
* PhishTank
* GeoLite
* OpenAlex

### Features Used

* Domain reputation
* DNS/IP intelligence
* Threat indicators
* URL patterns
* Hosting metadata
* Geolocation features

---

## Stage 2 — Site Type Classification Model

This model classifies trusted websites into categories based on raw URL/site-type data.

### Model Details

* Model: Logistic Regression
* Dataset Size: 18.6 GB
* Accuracy: ~70%
* Weighted F1-Score: 68.8%

### Purpose

* Website categorization
* Content/domain understanding
* Safe browsing intelligence

---

# Tech Stack

* Python
* Scikit-learn
* Pandas
* NumPy
* Gradient Boosting
* Logistic Regression

---

# Workflow

Input URL
↓
Reputation Classification
↓
If Safe → Site Type Classification
↓
Final Prediction Output

---

# Example Input

```python
url = "https://example.com"
```

# Example Output

```python
{
  "reputation": "Benign",
  "confidence_score": 0.98,
  "site_type": "Educational"
}
```

---

# Project Highlights

* Two-stage ML architecture
* Real-world threat intelligence integration
* High reputation detection accuracy
* Large-scale dataset training
* Cybersecurity-focused ML pipeline

---

# Future Improvements

* Deep Learning integration
* Real-time API deployment
* Browser extension support
* Live threat intelligence updates
* Transformer-based URL embeddings

---

# Installation

```bash
git clone <your-repo-link>
cd DOCC-URL-Classification-System
pip install -r requirements.txt
```

---

# Author

Krishak Josh

Machine Learning & Cybersecurity Enthusiast
