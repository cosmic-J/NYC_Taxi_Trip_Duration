# Urban Mobility Analysis and Trip Duration Prediction

Predicts NYC taxi trip duration using Linear Regression, classifies trips by duration using Logistic Regression, and finds pickup hotspots using K-Means clustering.

## Dataset
NYC Taxi Trip Duration (Kaggle): https://www.kaggle.com/datasets/yasserh/nyc-taxi-trip-duration
- 1,458,644 trips, 11 columns; a random sample of 50,000 rows is used.
- Download `NYC.csv` and place it in the same folder as the notebook.

## Concepts covered
- **Regression:** Linear Regression predicts trip duration (seconds).
- **Classification:** Logistic Regression predicts whether a trip is short, medium or long.
- **Clustering:** K-Means groups pickup locations into hotspots.

## What the project does
1. Load and sample the data
2. Clean it (remove unrealistic durations and out-of-bounds GPS points)
3. Descriptive statistics (mean, median, mode, std dev, variance, quartiles)
4. Feature engineering (Haversine distance, pickup hour, day of week)
5. Correlation analysis
6. Train a Linear Regression model (80/20 split) and form the regression equation
7. Evaluate with MAE, RMSE and R2, then plot actual vs predicted
8. Predict a new trip
9. Classification: split trip duration into short / medium / long (equal-sized groups), train Logistic Regression, evaluate with accuracy, classification report and confusion matrix
10. Clustering: choose k with the elbow method, run K-Means on pickup latitude/longitude, plot the hotspot clusters and compare average trip duration per cluster

## Results
**Regression**
- MAE: 284.11 s | RMSE: 414.16 s | R2: 0.6045
- Distance is the strongest predictor of trip duration.

**Classification**
- Accuracy: ~0.67 (chance level for 3 balanced classes is ~0.33)
- Short and long trips are predicted best; medium trips are the hardest to separate.

**Clustering**
- K = 5 pickup hotspots found with K-Means.
- Clusters far from central Manhattan have much longer average trip durations.

## How to run
pip install -r requirements.txt
Open `nyc_setter_commented.ipynb` and run all cells.

## Author
Jeevika S.
