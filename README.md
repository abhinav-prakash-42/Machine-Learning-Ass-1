### README

#### **Linear Regression with Gradient Descent**

This repository provides a Python implementation of linear regression using various gradient descent methods: **batch**, **stochastic**, and **mini-batch**. It demonstrates how different learning rates and gradient descent strategies affect the model's convergence and overall performance.

---

### **Files**
- **`src.ipynb`**: The Python script containing the implementation of linear regression and gradient descent.
- **`linearX.csv`**: Contains the feature values (X).
- **`linearY.csv`**: Contains the target values (Y).
- **Generated Graphs**:
  - `fig_cost_batch_<alpha>.png`: Cost vs. iteration graph for batch gradient descent.
  - `fig_regression_batch_<alpha>.png`: Regression fit graph for batch gradient descent.
  - `fig_cost_stochastic_<alpha>.png`: Cost vs. iteration graph for stochastic gradient descent.
  - `fig_cost_mini-batch_<alpha>.png`: Cost vs. iteration graph for mini-batch gradient descent.

---

### **Prerequisites**
- Python 3.x
- Required Libraries:
  - NumPy
  - Pandas
  - Matplotlib

Install the dependencies using:
```bash
pip install numpy pandas matplotlib
```

---

### **Code Overview**

#### **Functions**
1. **`cost_function(theta_0, theta_1, X, y)`**:  
   Computes the Mean Squared Error (MSE) cost function.

2. **`gradient_descent(X, y, theta_0, theta_1, alpha, iterations, method='batch', batch_size=1)`**:  
   Performs gradient descent. Supports:
   - `batch`
   - `stochastic`
   - `mini-batch` (requires `batch_size`).

3. **`predict(X, theta_0, theta_1)`**:  
   Predicts values using the fitted linear regression model.

4. **`normalize(X)`**:  
   Normalizes the input feature for better performance during optimization.

5. **`plot_data(alpha, iterations, method='batch', batch_size=1)`**:  
   Plots cost vs. iterations and regression fit for the given gradient descent method.

---

### **Usage**

1. **Run the Code**:  
   Execute the script to perform linear regression using batch, stochastic, and mini-batch gradient descent:
   ```bash
   python main.py
   ```

2. **Graphs Generated**:  
   - **Cost vs. Iterations**: Visualizes the cost function's behavior across iterations.
   - **Regression Fit**: Shows the linear regression line and how it fits the dataset.

3. **Key Parameters**:
   - **Learning Rate (`alpha`)**: Controls the step size in gradient descent.
   - **Iterations**: Number of updates to optimize the model.
   - **Method**: Gradient descent type (`batch`, `stochastic`, `mini-batch`).

---

### **Results**

1. **Learning Rate Analysis**:
   - \( \alpha = 0.005 \): Slow convergence.
   - \( \alpha = 0.5 \): Optimal convergence.
   - \( \alpha = 5 \): Diverges or oscillates.

2. **Gradient Descent Methods**:
   - **Batch**: Stable and consistent convergence.
   - **Stochastic**: Faster updates but noisy.
   - **Mini-Batch**: Balanced approach with faster convergence and reduced noise.

---

### **Customization**
- Update `alpha`, `iterations`, and `method` in the `plot_data` function to test various configurations.
- Modify `batch_size` for mini-batch gradient descent.

---

### **References**
- Linear regression and gradient descent concepts from machine learning courses.
- Python libraries for data analysis and visualization.

---

Feel free to explore and modify the code for deeper insights into gradient descent and linear regression!
