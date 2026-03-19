## 1. Prompt Given to AI

"Explain types of machine learning, regression, and classification with Python examples using Pandas."

---

## 2. AI Output (Summary)

The AI explained that machine learning has three main types: supervised learning, unsupervised learning, and reinforcement learning. It also explained regression and classification as types of supervised learning.

- **Supervised Learning**: Uses labeled data (example: predicting house prices)
- **Unsupervised Learning**: Finds patterns in unlabeled data (example: clustering customers)
- **Reinforcement Learning**: Learns using rewards and penalties (example: game AI)

It also explained:
- **Regression**: Used for predicting continuous values
- **Classification**: Used for predicting categories

### Example Code:

```python
import pandas as pd
from sklearn.datasets import load_iris
from sklearn.linear_model import LinearRegression, LogisticRegression

# Load dataset
iris = load_iris()
df = pd.DataFrame(iris.data, columns=iris.feature_names)
df['species'] = iris.target

# Convert target
df['species'] = df['species'].map({0:'setosa', 1:'versicolor', 2:'virginica'})

# Regression Example
X_reg = df[['petal length (cm)']]
y_reg = df['sepal length (cm)']

reg_model = LinearRegression()
reg_model.fit(X_reg, y_reg)

# Classification Example
X_clf = df[['petal length (cm)', 'petal width (cm)']]
y_clf = df['species']

clf_model = LogisticRegression(max_iter=200)
clf_model.fit(X_clf, y_clf)
