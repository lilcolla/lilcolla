import pandas as pd
import matplotlib.pyplot as plt

# Step 1: Load data
df = pd.read_csv("sales_data.csv")

# Step 2: Data Analysis
monthly_sales = df.groupby('month')['sales'].sum()

# Step 3: Data Visualization
plt.figure(figsize=(10, 6))
monthly_sales.plot(kind='bar')
plt.title('Monthly Sales Analysis')
plt.xlabel('Month')
plt.ylabel('Total Sales')
plt.savefig('monthly_sales.png')

print("Data analysis and visualization completed!")
