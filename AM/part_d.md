# 📊 Data Analysis using Pandas and Matplotlib

## 1. Prompt Given to AI

"Explain how to perform data analysis using Pandas and visualization using Matplotlib with examples."

---

## 2. AI Output (Summary)

The AI explained that Pandas is used for data manipulation and analysis, while Matplotlib is used for data visualization. It also provided examples like loading data, filtering, grouping, and plotting graphs such as histogram, bar chart, and line chart.

### Example Code:

```python
import pandas as pd
import matplotlib.pyplot as plt

# Create sample data
data = {
    'Name': ['A', 'B', 'C', 'D'],
    'Marks': [70, 85, 60, 90]
}

df = pd.DataFrame(data)

# Basic analysis
print(df.describe())

# Plot bar chart
plt.bar(df['Name'], df['Marks'])
plt.title("Marks of Students")
plt.xlabel("Name")
plt.ylabel("Marks")
plt.show()
