## Project Overview
This project develops machine learning models to predict PFAS (Per- and Polyfluoroalkyl Substances) contamination levels in U.S. water systems for 2024 using historical data from 2001 to 2023. The project employs time series analysis and machine learning techniques to capture patterns in PFAS contamination.

## Current Progress
- ✅ Initial data loading and preprocessing implemented
- ✅ Basic feature engineering completed
- ✅ Preliminary model development with XGBoost
- ✅ Basic prediction functionality for key PFAS compounds
- ✅ Initial MAE metrics for model evaluation

## Project Structure
```
├── data/
│   └── UCMR_data.csv
├── notebooks/
│   └── PFAS_Analysis.ipynb
├── src/
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   └── model.py
├── requirements.txt
└── README.md
```

## Current Results
Current model predictions for key PFAS compounds:

|
 Compound 
|
 MRL (μg/L) 
|
 MAE 
|
 Prediction Range 
|
|
----------
|
------------
|
-----
|
------------------
|
|
 PFOA 
|
 0.004000 
|
 0.001669 
|
 ~0.003366 
|
|
 PFOS 
|
 0.004000 
|
 0.001668 
|
 ~0.003184 
|
|
 PFHxS 
|
 0.003000 
|
 0.001699 
|
 ~0.002439 
|
|
 PFNA 
|
 0.004000 
|
 0.001582 
|
 ~0.003103 
|
|
 PFBS 
|
 0.003000 
|
 0.004998 
|
 ~0.002850 
|

## Technologies Used
- Python 3.8+
- pandas
- numpy
- scikit-learn
- XGBoost
- matplotlib/seaborn

## To-Do List
1. **Data Analysis**
   - [ ] Implement comprehensive EDA
   - [ ] Add regional analysis
   - [ ] Create data visualizations

2. **Feature Engineering**
   - [ ] Add seasonal components
   - [ ] Include geospatial features
   - [ ] Create advanced lag variables

3. **Model Improvements**
   - [ ] Implement additional models (LSTM, Random Forest)
   - [ ] Add cross-validation
   - [ ] Enhance prediction intervals

4. **Analysis**
   - [ ] Regional performance analysis
   - [ ] Feature importance analysis
   - [ ] Error analysis by region

5. **Visualization**
   - [ ] Interactive dashboard
   - [ ] Regional map visualizations
   - [ ] Trend analysis plots

## Project Requirements (Based on Course Instructions)
1. **Data Usage**
   - Historical data from 2001-2023
   - UCMR 1-4 Data
   - UCMR 5 Data (2023)
   - EPA Envirofacts

2. **Model Requirements**
   - Time series analysis
   - Forecasting for 2024
   - Regional analysis

3. **Evaluation Metrics**
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)
   - Regional performance analysis

## Installation & Setup
```bash
# Clone the repository
git clone [your-repo-url]

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install requirements
pip install -r requirements.txt
```

## Usage
```python
# Example code for basic usage
from src.model import PFASPredictor

# Initialize predictor
predictor = PFASPredictor()

# Load and prepare data
X, y = predictor.prepare_features(df, 'PFOA')

# Train model
model, mae = predictor.train_model(X, y)

# Generate predictions
predictions = predictor.predict_2024(model, mrl)
```

## Current Limitations
1. Predictions show limited seasonal variation
2. Regional analysis not yet implemented
3. Need to incorporate more sophisticated feature engineering
4. Error analysis needs expansion
5. Visualization components pending

## Next Steps
1. Implement regional analysis functionality
2. Add seasonal components to predictions
3. Create comprehensive visualization dashboard
4. Expand error analysis
5. Add LSTM model implementation

## Contributors
- Anudeep Adiraju
- Course: AI Practicum
- University: The University of Texas at San Antonio

## License
Apache 2.0

## Acknowledgments
- EPA for UCMR data
- UTSA AI Practicum course staff

---
Last Updated: November 13, 2024
