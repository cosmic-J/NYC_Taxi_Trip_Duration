# Urban Mobility Analysis and Trip Duration Prediction

Predicts NYC taxi trip duration using Linear Regression.

## Dataset
NYC Taxi Trip Duration (Kaggle): https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration
- 1,458,644 trips, 11 columns; a random sample of 50,000 rows is used.
- Download `NYC.csv` and place it in the same folder as the notebook.

## What the project does
1. Load and sample the data
2. Clean it (remove unrealistic durations and out-of-bounds GPS points)
3. Descriptive statistics (mean, median, mode, std dev, variance, quartiles)
4. Feature engineering (Haversine distance, pickup hour, day of week)
5. Correlation analysis
6. Train a Linear Regression model (80/20 split) and form the regression equation
7. Evaluate with MAE, RMSE and R2, then plot actual vs predicted
8. Predict a new trip

## Results
- MAE: 284.11 s | RMSE: 414.16 s | R2: 0.6045
- Distance is the strongest predictor of trip duration.

## How to run
pip install -r requirements.txt
Open `nyc_setter_commented.ipynb` and run all cells.

## Author
Jeevika S.