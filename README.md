# Spotify Tracks Analytics & Clustering using PySpark

This repository contains the complete big data analysis and machine learning pipeline utilizing Apache Spark (PySpark) to process, analyze, and cluster a large-scale dataset of Spotify tracks.

---

## 📌 Project Overview
As music streaming platforms grow exponentially, handling and extracting insights from massive datasets requires distributed computing frameworks. This project leverages **Apache Spark (PySpark)** and **Spark MLlib** to perform end-to-end Big Data analytics—ranging from distributed data cleaning and exploratory data analysis (EDA) to unsupervised machine learning segmentation (K-Means Clustering).

---

## ⚙️ Key Methodologies & Workflow
1. **Data Understanding & Ingestion:** Loaded and inspected a large-scale dataset consisting of over 114,000 tracks with multiple attributes using PySpark DataFrames.
2. **Data Cleaning & Preprocessing:** Handled missing values, removed duplicates, converted data types safely, and eliminated invalid numeric records.
3. **Exploratory Data Analysis (EDA):** Analyzed genre popularity distribution, explicit vs. non-explicit track ratios, top artists representation, and core audio characteristics of popular songs.
4. **Machine Learning (K-Means Clustering):** 
   * Selected numeric audio features (such as `popularity`, `danceability`, `energy`, `acousticness`, `instrumentalness`, `liveness`, `valence`, and `tempo`).
   * Built a feature pipeline using `VectorAssembler` and `StandardScaler`.
   * Trained an unsupervised **K-Means Clustering** model using Spark MLlib and evaluated cluster separation via the **Silhouette Score**.

---

## 📊 Key Findings & Insights
* **Genre Popularity:** Specific music genres emerged with distinct average popularity ratings across the distributed dataset.
* **Content Safety:** The vast majority of the tracks are classified and filtered based on explicit content parameters.
* **Audio Characteristics:** Highly popular songs exhibit correlated audio profiles regarding energy, danceability, and acousticness levels.
* **Clustering Performance:** The K-Means model successfully segmented the tracks into distinct clusters, effectively differentiating audio profiles for music recommendation strategies.

---

## 🛠️ Tech Stack & Tools
* **Big Data Framework:** Apache Spark (PySpark), Spark MLlib
* **Environment:** Google Colab
* **Data Processing & Visualization:** Pandas, Matplotlib
* **Language:** Python

---

## 📁 Repository Structure
```text
├── dataset/            # Dataset reference/links
├── notebooks/          # PySpark Jupyter Notebooks (.ipynb)
├── reports/            # Official Big Data Project Report (PDF)
└── outputs/            # Visualizations and EDA charts
