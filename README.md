# Project : Customer Segmentation Analysis

**Objective:** Conduct customer segmentation to enhance marketing strategies and improve customer targeting.

## Data Collection

- **Data Source:** `customer_data.csv`
- **Sample Data:**

    ```plaintext
    CustomerID,Age,AnnualIncome,SpendingScore
    1,25,50000,60
    2,45,80000,70
    3,30,60000,55
    4,35,70000,75
    ```

## Data Cleaning

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
