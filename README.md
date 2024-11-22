# Customer Segmentation Using K-Means Clustering

This project segments customers into distinct groups based on their **Annual Income** and **Spending Score** using the **K-Means Clustering** algorithm.

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Technologies Used](#technologies-used)  
3. [Dataset](#dataset)  
4. [Installation Guide](#installation-guide)  
5. [Usage](#usage)  
6. [Model Evaluation and Visualization](#model-evaluation-and-visualization)  
7. [License](#license)  

## Project Overview

Customer segmentation helps businesses target their customers more effectively by categorizing them into distinct groups. This project uses **K-Means Clustering** to segment customers into five clusters. The results are visualized in a scatter plot, showing clear distinctions between customer groups.

### Objectives:
- Determine the optimal number of clusters using the **Elbow Method**.  
- Segment customers into 5 groups based on clustering results.  
- Visualize the clusters and their centroids.  

## Technologies Used

- **Python**: Programming language used for analysis and visualization.  
- **Scikit-learn**: For implementing the K-Means clustering algorithm.  
- **Matplotlib**: For visualizing the clusters and centroids.  
- **NumPy**: For numerical computations.  

## Dataset

The dataset consists of customer data with the following attributes:
- `CustomerID`: Unique ID for each customer.  
- `Gender`: Gender of the customer.  
- `Age`: Age of the customer.  
- `Annual Income`: Annual income in thousands of dollars.  
- `Spending Score`: A score between 1–100, assigned based on customer behavior and spending patterns.  

This project focuses on **Annual Income** and **Spending Score** as clustering features.


## Usage

1. **Load the Dataset**:  
   Ensure the dataset (`Mall_Customers.csv`) is in the project directory. Load it using:  
   ```python
   dataset = pd.read_csv('Mall_Customers.csv')
   X = dataset.iloc[:, [3, 4]].values
   
### Run the Clustering Script
Execute the script to perform clustering and visualize the results:
```bash
python src/kmeans_clustering.py

### Visualize Results

The script generates the following visualizations:

1. **Elbow Method Graph**: Helps determine the optimal number of clusters.
2. **Cluster Scatter Plot**: Displays customer groups and centroids.

### Model Evaluation and Visualization

#### Elbow Method
Plots the **WCSS (Within-Cluster Sum of Squares)** for different numbers of clusters to find the "elbow point."

```python
# Elbow Method Graph
plt.figure(figsize=(8, 6))
plt.plot(range(1, 11), wcss, marker='o', linestyle='--', color='blue')
plt.title('The Elbow Point Graph')
plt.xlabel('Number of Clusters')
plt.ylabel('WCSS')
plt.grid(True)
plt.show()

## Clusters:
Cluster 1: Green
Cluster 2: Red
Cluster 3: Yellow
Cluster 4: Violet
Cluster 5: Blue
Centroids: Displayed as cyan points marked with "x".
