# pm10_prediction

A package for PM10 prediction from data cleaning to prediction.

## Installation

!pip install aju_pm10_hourly_prediction


# run the code
from aju_pm10_hourly_prediction import run_full_pipeline

# Path to your test data and models
input_csv = 'your/path/data/raw_data.csv'
xgb_model_path = 'your/path/models/best_xgb_model2.pkl'
rf_model_path = 'your/path/models/best_rf_model.pkl'
svm_model_path = 'your/path/models/best_svm_model.pkl'
gru_model_path = 'your/path/models/gru_model.h5'
lstm_model_path = 'your/path/models/lstm_model.keras'

# Run the full pipeline
pred_df = run_full_pipeline(
    input_csv=input_csv, 
    xgb_model_path=xgb_model_path,
    rf_model_path=rf_model_path,
    svm_model_path=svm_model_path,
    gru_model_path=gru_model_path,
    lstm_model_path=lstm_model_path
)

# Display the results
pred_df
