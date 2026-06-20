# Smart Irrigation Requirement Prediction

This project predicts whether irrigation is required from smart farming sensor data. The target is derived from soil moisture, temperature, rainfall, humidity, sunlight, and NDVI readings.

## Workflow

- Load local smart farming sensor data
- Create a `water_score`
- Convert the score into a binary `irrigation_required` target
- Benchmark SVM, KNN, and CatBoost classifiers
- Evaluate the best model
- Review feature importance
- Run one example prediction

## Models

- SVM
- KNN
- CatBoost

## Results

On the current train/test split:

| Model | Accuracy | Precision | Recall | F1 |
| --- | ---: | ---: | ---: | ---: |
| KNN | 0.9600 | 0.9600 | 0.9600 | 0.9600 |
| CatBoost | 0.9500 | 0.9787 | 0.9200 | 0.9485 |
| SVM | 0.9100 | 0.8868 | 0.9400 | 0.9126 |

Best model: `KNN`

## Files

```text
Smart_Irrigation_Water_Need_Prediction.ipynb
data/
  smart_farming_sensor_data.csv
README.md
```


## How to Run

Install the required packages:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn catboost
```

Open and run:

```text
Smart_Irrigation_Water_Need_Prediction.ipynb
```
