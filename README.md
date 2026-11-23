
# EdgeTwin-XAI
## Explainable AI-Powered Predictive Maintenance and Industrial Digital Twin System

### Project Overview

EdgeTwin-XAI is an AI-powered predictive maintenance system designed to monitor industrial equipment, predict potential machine failures, and support proactive maintenance decisions.

The project combines machine learning, explainable artificial intelligence (XAI), and digital twin analytics to provide machine health assessments, failure risk predictions, root cause explanations, and maintenance recommendations.

The system uses XGBoost for failure prediction, SHAP for model explainability, and interactive visualizations for monitoring machine performance.

---

## Problem Statement

Unexpected industrial equipment failures can result in costly downtime, increased maintenance expenses, and reduced operational efficiency.

Traditional maintenance approaches often rely on fixed schedules or reactive repairs, which may not accurately reflect the condition of individual machines.

EdgeTwin-XAI addresses these challenges by developing a data-driven predictive maintenance framework that identifies potential failures, evaluates machine health, and supports informed maintenance planning.

---

## Project Objectives

- Develop a machine learning model to predict industrial equipment failures.
- Monitor machine health using digital twin representations.
- Identify important factors contributing to failure predictions.
- Estimate Remaining Useful Life (RUL).
- Classify machines according to failure risk and maintenance priority.
- Provide explainable predictions using SHAP.
- Visualize machine health and fleet-level performance.
- Support preventive maintenance through risk-based recommendations.

---

## Dataset

**Dataset:** AI4I 2020 Predictive Maintenance Dataset

The dataset contains 10,000 machine records representing industrial operating conditions and failure events.

### Input Features

- Air Temperature
- Process Temperature
- Rotational Speed
- Torque
- Tool Wear
- Machine Type

### Prediction Targets

- Machine Failure
- Tool Wear Failure (TWF)
- Heat Dissipation Failure (HDF)
- Power Failure (PWF)
- Overstrain Failure (OSF)
- Random Failure (RNF)

The dataset is used to train and evaluate machine learning models for predictive maintenance.

---

## Technologies Used

| Category | Technologies |
|----------|--------------|
| Programming | Python |
| Machine Learning | XGBoost, Scikit-learn |
| Data Balancing | SMOTE |
| Explainable AI | SHAP |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Interactive Components | IPython Widgets |
| Graph Visualization | NetworkX |
| Development Environment | Jupyter Notebook, VS Code |

---

## Key Features

### 1. Machine Failure Prediction

Uses an XGBoost classification model to estimate the probability of industrial machine failure.

SMOTE is applied to the training data to address class imbalance.

### 2. Explainable AI Using SHAP

SHAP explanations help identify the machine parameters that contribute to model predictions.

The system provides global feature importance and individual prediction explanations.

### 3. Digital Twin Monitoring

Creates machine-level digital twin records containing:

- Machine ID
- Health Score
- Failure Probability
- Operational Status
- Risk Segment
- Maintenance Priority
- Alert Level

### 4. Failure Mode Analysis

Analyzes different failure modes, including:

- Tool Wear Failure
- Heat Dissipation Failure
- Power Failure
- Overstrain Failure
- Random Failure

The system also identifies influential features associated with predicted risks.

### 5. Remaining Useful Life Estimation

Estimates Remaining Useful Life (RUL) to support maintenance scheduling.

RUL values are model-derived estimates and should not be interpreted as validated physical lifetime predictions.

### 6. Maintenance Prioritization

Ranks machines based on:

- Failure Probability
- Health Score
- Remaining Useful Life

This helps identify machines requiring earlier maintenance attention.

### 7. Fleet Analytics Dashboard

Provides visualizations and summaries of:

- Average Fleet Health
- Average Failure Risk
- Average Remaining Useful Life
- Critical Machines
- Emergency Alerts
- Maintenance Priorities

### 8. Real-Time Monitoring Simulation

Includes a simulated machine monitoring workflow that demonstrates changing operating conditions and their effects on predicted health and failure risk.

This is a simulation rather than a live industrial sensor deployment.

### 9. What-If Maintenance Analysis

Includes an interactive maintenance scenario analysis tool.

It compares preventive maintenance with delayed maintenance using assumed cost parameters to illustrate potential cost avoidance.

The financial results are illustrative estimates, not measured industrial savings.

---

## Project Workflow

1. Load the AI4I 2020 dataset.
2. Clean and preprocess machine operating data.
3. Encode machine types and prepare features.
4. Split data into training and testing sets.
5. Apply SMOTE to the training data.
6. Train the XGBoost failure prediction model.
7. Evaluate model performance.
8. Generate SHAP explanations.
9. Estimate machine health and failure risks.
10. Generate digital twin records.
11. Rank maintenance priorities.
12. Visualize fleet analytics and machine-level results.
13. Run monitoring and maintenance simulations.
14. Export results to CSV.

---

## Model Evaluation

The notebook evaluates model performance using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix
- Precision-Recall Analysis

Actual evaluation results should be taken from the executed notebook outputs.

---

## Project Structure

```text
EdgeTwin-XAI/
|
|-- EdgeTwin_XAI.ipynb
|-- README.md
|-- requirements.txt
|
|-- data/
|   |-- ai4i2020.csv
|
|-- outputs/
|   |-- EdgeTwin_XAI_Final.csv
|
|-- dashboards/
|
|-- screenshots/
```

The structure above is recommended. Include folders only when their corresponding files are available.

---

## Installation and Execution

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/EdgeTwin-XAI.git
```

### Step 2: Navigate to the Project Folder

```bash
cd EdgeTwin-XAI
```

### Step 3: Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 4: Prepare the Dataset

Download the AI4I 2020 Predictive Maintenance Dataset and save it as:

```text
ai4i2020.csv
```

The notebook currently expects this file in its working directory.

If the dataset is stored in the `data` folder, update the notebook's `DATA_PATH` variable accordingly.

### Step 5: Run the Notebook

Open `EdgeTwin_XAI.ipynb` in Jupyter Notebook or VS Code.

Execute the cells sequentially to train the models, generate predictions, visualize results, and export the digital twin data.

---

## Output

The system generates:

```text
EdgeTwin_XAI_Final.csv
```

The exported dataset contains 10,000 machine records and 18 columns.

It includes machine health scores, failure probabilities, risk segments, failure mode predictions, RUL estimates, root cause information, and maintenance-related fields.

---

## Applications

- Industrial Predictive Maintenance
- Smart Manufacturing
- Equipment Health Monitoring
- Industrial Digital Twin Analytics
- Explainable AI for Manufacturing
- Risk-Based Maintenance Planning

---

## Future Enhancements

- Integration with real industrial IoT sensors.
- Deployment as a standalone web application.
- Cloud-based machine monitoring.
- Real-time alert notification systems.
- Improved RUL estimation using time-series data.
- Validation using real industrial maintenance records.

---

## Conclusion

EdgeTwin-XAI demonstrates how machine learning, explainable AI, and digital twin analytics can be combined to support intelligent predictive maintenance.

The project provides a framework for identifying machine failure risks, understanding model predictions, monitoring equipment health, and prioritizing maintenance activities.

Its objective is to support more transparent and proactive industrial maintenance decisions.
