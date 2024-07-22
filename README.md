# Project : Customer Segmentation Analysis

**Objective:** Conduct customer segmentation to enhance marketing strategies and improve customer targeting.

## 1. Data Collection

- **Data Source:** `customer_data.csv`

## 2. Data Cleaning

**Using Python (Pandas):**

```python
import pandas as pd

# Load data
df = pd.read_csv('customer_data.csv')

# Display the first few rows
print(df.head())

# Check for missing values
print(df.isnull().sum())

# Fill or drop missing values if any
df = df.dropna()
```
![image](https://github.com/user-attachments/assets/2e42cb1b-b268-4052-9345-0822a6cc69f8)

## 3. Segmentation Analysis

**Using Python (K-means Clustering):**

```python
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt

# Select features for clustering
X = df[['Age', 'AnnualIncome', 'SpendingScore']]

# Apply K-means clustering
kmeans = KMeans(n_clusters=3, random_state=0).fit(X)
df['Cluster'] = kmeans.labels_

# Plot clusters
plt.scatter(df['AnnualIncome'], df['SpendingScore'], c=df['Cluster'], cmap='viridis')
plt.xlabel('Annual Income')
plt.ylabel('Spending Score')
plt.title('Customer Segmentation')
plt.show()
```

![image](https://github.com/user-attachments/assets/ba7a3744-73f8-4c70-95a4-01b396e09c3f)

## 4. Data Visualization

**Using Matplotlib (Python):**
```python 
import matplotlib.pyplot as plt

# Scatter plot of customer segments
plt.scatter(df['Age'], df['AnnualIncome'], c=df['Cluster'], cmap='viridis')
plt.xlabel('Age')
plt.ylabel('Annual Income')
plt.title('Customer Segmentation')
plt.show()
```
![image](https://github.com/user-attachments/assets/9abea56c-bdd3-4443-a37c-5a7b02ce9197)

## 5. Reporting

**Customer Segmentation Analysis Report**

- **Segments Identified:** 3 distinct customer segments based on age, income, and spending score.
- **Segment Profiles:** 
  - Segment 1: Young, high-income, high-spending.
  - Segment 2: Middle-aged, moderate-income, moderate-spending.
  - Segment 3: Older, lower-income, low-spending.
- **Recommendations:** Tailor marketing strategies for each segment based on their profiles.

