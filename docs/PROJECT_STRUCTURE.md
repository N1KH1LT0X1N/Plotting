# Project Structure Documentation

## Directory Overview

### `/eda` - Exploratory Data Analysis
Year-specific FIFA dataset analysis notebooks (2017-2023).

**Files:**
- `eda17.ipynb` through `eda23.ipynb` - Individual year analysis
- Each notebook contains:
  - Data loading and inspection
  - Missing value analysis
  - Statistical summaries
  - Distribution plots
  - Correlation analysis
  - Feature engineering

### `/final_steps` - Final Analysis & Models
Consolidated analysis and machine learning models.

**Files:**
- `eda.ipynb` - Comprehensive EDA across all years
  - Comprehensive FIFA Wage Prediction EDA class
  - Multi-phase analysis (7 phases)
  - Interactive Plotly visualizations
  - Temporal trend analysis (2017-2022)
  
- `model.ipynb` - Machine Learning models
  - Random Forest Regressor
  - Linear Regression
  - Feature importance analysis
  - Model evaluation metrics

### `/fifa_dataset` - Raw Data
Original FIFA CSV files (2017-2023). **Not tracked in Git due to size.**

### `/fifa_dataset_cleaned` - Processed Data
Cleaned and merged datasets ready for analysis.

**Files:**
- `merging.ipynb` - Data consolidation notebook
- `fifa_training_2017_2022.csv` - Training dataset
- `fifa_final21.csv` - FIFA 21 cleaned data

### `/Interactive Controls` - Interactive Visualizations
Plotly-based interactive dashboard demos.

## Key Notebooks

### 1. EDA Notebooks (`eda/`)
**Purpose**: Year-by-year exploratory data analysis of FIFA datasets

**Key Analyses:**
- Data structure inspection
- Null value patterns
- Distribution analysis
- Position-wise statistics
- Body type extraction
- Value/wage trends

### 2. Final EDA (`final_steps/eda.ipynb`)
**Purpose**: Comprehensive cross-year analysis with ML focus

**Features:**
- FIFAWageEDA class with 7 analysis phases
- Overview & target variable analysis
- Correlation matrices
- Position-specific insights
- Temporal trends (2017-2022)
- Geographic analysis
- Advanced pattern recognition
- ML preparation insights

### 3. Model Notebook (`final_steps/model.ipynb`)
**Purpose**: Wage prediction machine learning models

**Models Implemented:**
- Linear Regression (baseline)
- Random Forest Regressor
- Feature importance analysis
- Cross-validation
- Performance metrics (RMSE, R², MAE)

## Data Flow

```
Raw FIFA CSVs (fifa_dataset/)
    ↓
Individual EDA (eda/*.ipynb)
    ↓
Data Cleaning & Merging (fifa_dataset_cleaned/merging.ipynb)
    ↓
Cleaned Datasets (fifa_dataset_cleaned/*.csv)
    ↓
Final EDA (final_steps/eda.ipynb)
    ↓
ML Models (final_steps/model.ipynb)
```

## Naming Conventions

- **Notebooks**: Lowercase with underscores or descriptive names
- **Datasets**: Descriptive names with year/version indicators
- **Variables**: snake_case for Python, PascalCase for classes
- **Functions**: Descriptive verbs (e.g., `load_data`, `clean_body_type`)

## Dependencies

See `requirements.txt` for full list. Key libraries:
- pandas, numpy - Data manipulation
- matplotlib, seaborn, plotly - Visualization
- scikit-learn - Machine learning
- skimpy, summarytools - Statistical summaries

## Running the Analysis

1. Start with `eda/eda21.ipynb` (or any year) to understand single-year analysis
2. Review `fifa_dataset_cleaned/merging.ipynb` for data consolidation approach
3. Explore `final_steps/eda.ipynb` for comprehensive multi-year insights
4. Run `final_steps/model.ipynb` for ML wage prediction models

## Contributing

When adding new notebooks:
1. Follow existing naming conventions
2. Add markdown documentation cells
3. Clear outputs before committing
4. Update this documentation
5. Add any new dependencies to `requirements.txt`
