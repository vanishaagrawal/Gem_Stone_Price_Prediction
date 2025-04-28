# Gemstone Price Prediction

## Problem Statement

```I discovered a dataset, "JewelStone," with details and prices for nearly 27,000 cubic stones. Using this data, the goal is to predict stone prices based on key attributes, helping to identify stones with higher profit potential. Additionally, finding the top five most important attributes could offer valuable insights for maximizing profits.```


## Dataset description

* Carat	- Carat weight of the gemstone.
* Cut - Describe the cut quality of the gemstone. Quality is increasing order Fair, Good, Very Good, Premium, Ideal.
* Color - Colour of the gemstone.With D being the best and J the worst.
* Clarity - Gemstone Clarity refers to the absence of the Inclusions and Blemishes. (In order from Best to Worst, FL = flawless, I3= level 3 inclusions) FL, IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3
* Depth	- The Height of a gemstone, measured from the Culet to the table, divided by its average Girdle Diameter.
* Table - The Width of the gemstone's Table expressed as a Percentage of its Average Diameter.
* Price	- the Price of the gemstone.
* X	- Length of the gemstone in mm.
* Y	- Width of the gemstone in mm.
* Z	- Height of the gemstone in mm.


### Create project template hierarchy
```bash
python template.py
```

### Setup development environment
```bash
bash init_setup.sh
```

### Acivate environment
```bash
source activate ./env
```

### Install project as local package
```bash
pip install -r requirement.txt
```

## Pipelines
### Training Pipeline
    * Data Ingestion (fetched data from source)
    * Data Transformation (Feature Engineering, Data Preprocessing)
    * Model Builing (Create a model using the processed data)

## MLFlow & DagsHub
Copy the values from DagsHub > Repo > Remote > Experiments

```bash
set MLFLOW_TRACKING_URI=<>
set MLFLOW_TRACKING_USERNAME=<>
set MLFLOW_TRACKING_PASSWORD<>
```
If the above are not set, then ML Experiments gets registered in local system else gets published to DagsHub

#### Command to train the pipeline
```bash
python src\GemstonePricePrediction\pipelines\training_pipeline.py
```

### Prediction Pipeline
    * Two types of prediction pipeline
        * Single record prediction
        * Batch prediction


## Explainer Dashboard

* Feature Importance
* Regression Stats
* Individual Predictions
* What if?
* Feature Dependence

```bash
python dashboard.py
```

## Flask App
```bash
python app.py
```

## Streamlit App
```bash
streamlit run streamlit_app.py
```

## Dataset Link
* https://www.kaggle.com/datasets/colearninglounge/gemstone-price-prediction
