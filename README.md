# Lift-logic-but-faster
Was irritated of slow and useless elevators in my hostel so made a project out of it

## Overview

LiftLogic is an elevator optimization project that combines rule-based optimization and machine learning (Random Forest) to minimize elevator energy costs and improve efficiency.
The project is implemented as a Google Colab notebook for easy, interactive experimentation and visualization.

## Features

- **Data Handling:**  
  - 80% of the data is used for training, 20% for testing.
- **Rule-Based Optimization:**  
  - Elevators are rewarded for moving downward (less energy cost) and penalized for moving upward (higher energy cost).
  - Cost function:
    - **If going down:**  
      `weight_cost = n1 * floor_diff * weight_factor`
    - **If going up:**  
      `weight_cost = n2 * floor_diff * weight_factor`
    - Where `n1 = 0.7`, `n2 = 1.5`, and `weight_factor = 1 + weight_of_lift`.
- **Machine Learning:**  
  - Random Forest algorithm is used to predict rush hour periods and optimize elevator scheduling.
- **Visualization:**  
  - Generates plots and visualizations for model predictions and elevator performance.
- **ETA Prediction:**  
  - Configures and predicts estimated time of arrival for elevators.

## Requirements

- **Runs entirely in Google Colab.**
- Dependencies (automatically installed in Colab):
  - pandas
  - numpy
  - matplotlib
  - scikit-learn
  - scipy

## How to Use

1. **Open the notebook in Google Colab**  
   - Upload your dataset (in CSV, 24h format recommended) using the provided upload cell.
2. **Run all cells in order:**  
   - The notebook will:
     - Install dependencies if needed.
     - Prompt you to upload your dataset.
     - Split the data into train/test sets.
     - Train the Random Forest model for rush hour prediction.
     - Apply rule-based optimization to elevator movements.
     - Output performance metrics and visualizations.
3. **Review the results and visualizations**  
   - Analyze elevator efficiency and rush hour predictions directly in the notebook.

