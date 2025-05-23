# Predictive Maintenance for Industrial Equipment

## Project Overview
This project implements a predictive maintenance system to forecast equipment failures in industrial settings. The system leverages machine learning techniques to minimize operational downtime, reduce maintenance costs, and improve equipment reliability. Using a dataset of machine operational settings, sensor measurements, and historical failure records, the model predicts potential failures, enabling proactive maintenance.

## Key Features
- **Machine Learning Models**: Random Forest, Logistic Regression, and Support Vector Machine (SVM)
- **Feature Engineering**: Introduced new features like `temp_diff` (temperature difference) and `torque_speed_interaction`.
- **Data Preprocessing**: Handled missing values, removed duplicates, and standardized sensor data.
- **Model Evaluation**: Analyzed model performance using precision, recall, accuracy, and AUC-ROC.
- **Interactive Dashboard**: Integrated with Dash and Plotly for data visualization.

## Dataset
The dataset, sourced from the Microsoft Azure AI Gallery, contains:
- **10,000 rows** with **10 columns**.
- Includes machine operational settings, sensor readings (e.g., temperature, torque), and historical failure types.

**Dataset Link:** [Download Dataset](https://github.com/nandhu83/Predictive-Maintenance-For-Industrial-Equipment/blob/main/Datatset/predictive_maintenance.csv)

### Dataset Features
- `UDI`: Unique record identifier
- `Product ID`: Machine ID
- `Type`: Machine category (L, M, H)
- `Air temperature [K]` and `Process temperature [K]`
- `Rotational speed [rpm]` and `Torque [Nm]`
- `Tool wear [min]`
- `Target`: Binary failure indicator
- `Failure Type`: Type of failure (e.g., Heat Dissipation, Power Failure)

## Installation
To set up the environment, run the following commands:
```bash
# Clone the repository
git clone https://github.com/nandhu83/Predictive-Maintenance-For-Industrial-Equipment.git

# Navigate to the project directory
cd Predictive-Maintenance-For-Industrial-Equipment

# Install dependencies
pip install -r requirements.txt
```

### Required Libraries
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `plotly`
- `dash`

## Project Structure
```
.
├── Dataset
│   └── predictive_maintenance.csv
├── Notebook
│   └── Predictive Maintenance For Industrial Equipment.ipynb
├── Outputs
│   ├── predictive_maintenance_with_warnings.csv
│   └── predictive_maintenance_schedule.csv
├── Report and PPT
│   └── project_report.pptx
├── requirements.txt
└── README.md
```

## Usage
1. **Open the Jupyter Notebook:**
```bash
jupyter notebook Notebook/Predictive Maintenance For Industrial Equipment.ipynb
```
2. **Run the Cells Sequentially:**
   - Preprocessing the data
   - Training the models
   - Evaluating the models
   - Visualizing insights

## Model Performance
- **Random Forest**: High accuracy and robust feature handling.
- **SVM**: Effective in capturing complex patterns.
- **Logistic Regression**: Simple yet interpretable benchmark.

### Key Insights
- Tool wear and temperature differences are critical failure predictors.
- Torque-speed interaction significantly influences machine performance.

## Maintenance Strategies
- **Critical Risk**: Immediate action required.
- **Moderate Risk**: Schedule maintenance.
- **Low Risk**: Routine inspection.
