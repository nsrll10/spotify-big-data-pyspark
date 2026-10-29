# Spotify Tracks Analytics & Clustering using PySpark

This repository contains the complete big data analysis and machine learning pipeline utilizing Apache Spark (PySpark) to process, analyze, and cluster a large-scale dataset of 114,000 Spotify tracks[cite: 61, 62].

---

## 📌 Project Overview
As music streaming platforms grow exponentially, handling and extracting insights from massive datasets requires distributed computing frameworks. This project leverages **Apache Spark (PySpark)** and **Spark MLlib** to perform end-to-end Big Data analytics—ranging from distributed data cleaning and exploratory data analysis (EDA) to unsupervised machine learning segmentation (K-Means Clustering)[cite: 61, 63].

---

## ⚙️ Key Methodologies & Workflow
1. **Data Understanding & Ingestion:** Loaded and inspected a large-scale dataset of 114,000 tracks with 21 attributes using PySpark DataFrames[cite: 61, 62, 65].
2. **Data Cleaning & Preprocessing:** Handled missing values, removed duplicates, converted data types safely, and eliminated invalid numeric records[cite: 63, 66].
3. **Exploratory Data Analysis (EDA):** Analyzed genre popularity distribution, explicit vs. non-explicit track ratios, top artists representation, and core audio characteristics of popular songs[cite: 61, 63, 69, 70].
4. **Machine Learning (K-Means Clustering):** 
   * Selected numeric audio features (`popularity`, `danceability`, `energy`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`)[cite: 64, 71].
   * Built a feature pipeline using `VectorAssembler` and `StandardScaler`[cite: 64, 72].
   * Trained an unsupervised **K-Means Clustering** model ($k=4$) using Spark MLlib and evaluated cluster separation via the **Silhouette Score**[cite: 61, 64, 73].

---

## 📊 Key Findings & Insights
* **Genre Popularity:** Pop-film and K-pop genres emerged with the highest average popularity ratings[cite: 69].
* **Content Safety:** The vast majority of the tracks (91.4%) are classified as non-explicit[cite: 69, 70].
* **Audio Characteristics:** Highly popular songs generally exhibit elevated energy and danceability levels alongside lower acousticness[cite: 71].
* **Clustering Performance:** The K-Means model successfully segmented the tracks into 4 distinct clusters achieving a Silhouette Score of **0.3308**, effectively differentiating audio profiles for music recommendation strategies[cite: 73, 76].

---

## 🛠️ Tech Stack & Tools
* **Big Data Framework:** Apache Spark (PySpark), Spark MLlib[cite: 63]
* **Environment:** Google Colab[cite: 63]
* **Data Processing & Visualization:** Pandas, Matplotlib[cite: 63]
* **Language:** Python[cite: 63]

---

## 📁 Repository Structure
```text
├── dataset/            # Dataset reference/links
├── notebooks/          # PySpark Jupyter Notebooks (.ipynb)
├── reports/            # Official Big Data Project Report (PDF)
└── outputs/            # Visualizations and EDA charts
