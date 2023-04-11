
# Linear Regression

## Sample Code

### Import Libraries
```
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score
```

### Load Data
```
# Load data from CSV file
data = pd.read_csv("data.csv")

# Split data into input features and target variable
X = data.iloc[:, :-1]
y = data.iloc[:, -1]

```

### Create model
```
# Create a linear regression model object
lr_model = LinearRegression()

# Train the model on the training data
lr_model.fit(X_train, y_train)
```

### Evaluate model
```
# Make predictions on test data
y_pred = lr_model.predict(X_test)

# Calculate mean squared error (MSE)
mse = mean_squared_error(y_test, y_pred)

# Calculate coefficient of determination (R^2)
r2 = r2_score(y_test, y_pred)

```

### Plot results
```

# Plot the actual vs predicted values
plt.scatter(y_test, y_pred)
plt.xlabel("Actual Values")
plt.ylabel("Predicted Values")
plt.show()

```

### Predict New Values

```bibtex

# Predict new values using the trained model
new_data = np.array([4.5, 6.7, 8.9]).reshape(-1, 1)
new_predictions = lr_model.predict(new_data)


```