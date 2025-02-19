# Baker Hughes Challenge - Data Downsampling & Clustering  

## Overview  
This project explores **data downsampling techniques** for large datasets in the **Baker Hughes Challenge**, focusing on **uniform grid-based downsampling** and **high-density clustering-based downsampling** using **K-Means and Gaussian Mixture Models (GMM)**. The goal is to efficiently reduce dataset size while preserving its statistical properties.  

## Features  
- **Exploratory Data Analysis (EDA)**:  
  - Scatter plots, hexbin plots, and Kernel Density Estimation (KDE) for visualization.  
- **Selection #1: Uniform Coverage Downsampling**  
  - Uses **grid-based selection** to maintain even distribution.  
  - Nearest Neighbors analysis to evaluate uniformity.  
- **Selection #2: High-Density Region Downsampling**  
  - Uses **K-Means and GMM clustering** to retain high-density regions.  
  - Optimal cluster count determined using **Elbow Method (K-Means) and BIC (GMM)**.  
- **Comparison of Downsampling Methods**  
  - **Heatmap comparisons** of original and downsampled datasets.  
  - **Pearson correlation** to measure similarity in cluster density distributions.  

## Technologies Used  
- **Python Libraries**:  
  - `pandas`, `numpy` – Data processing  
  - `matplotlib`, `seaborn` – Visualization  
  - `scikit-learn` – Clustering & machine learning  
  - `scipy` – Spatial analysis  

## Data Processing Workflow  
1. **Load Dataset**: Read CSV file containing **frequency (FREQ) and power (POWER)** measurements.  
2. **EDA & Visualization**: Identify density regions using **scatter plots, hexbin plots, and KDE**.  
3. **Uniform Downsampling**:  
   - Normalize data and create a **grid-based selection**.  
   - Select data points evenly across grid cells.  
4. **High-Density Downsampling**:  
   - Use **K-Means Clustering** to group similar data points.  
   - Determine optimal clusters using **Elbow Method**.  
   - Apply **Gaussian Mixture Model (GMM)** for density estimation.  
5. **Comparison & Evaluation**:  
   - Visualize downsampled datasets against the original.  
   - Calculate **nearest neighbor distances**, **variance**, and **correlation** to assess data retention quality.  

## How to Run  
1. **Clone the Repository**  
   ```bash
   git clone https://github.com/yourusername/Baker-Hughes-Challenge.git
   cd Baker-Hughes-Challenge
