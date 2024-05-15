# Predicting-Forest-Fire-Impact: A-Machine-Learning-Approach-Using-UCI-Data


## Overview
This project aims to develop and evaluate predictive models for assessing the impact of forest fires using the Forest Fire dataset from the UCI Machine Learning Repository. The goal is to predict the area affected by forest fires based on various environmental and temporal factors.

## Data Source
Download the Forest Fire dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/162/forest+fires). Extract the files into the subdirectory:
(relative to the `./src/` directory).

## Data Description
The dataset contains the following variables, with descriptions derived from the accompanying `forestfires.names` file:

| Variable | Description                                  | Type       |
|----------|----------------------------------------------|------------|
| X        | X-axis spatial coordinate within the map     | Integer    |
| Y        | Y-axis spatial coordinate within the map     | Integer    |
| month    | Month of the year                            | Categorical|
| day      | Day of the week                              | Categorical|
| FFMC     | Fine Fuel Moisture Code index                | Float      |
| DMC      | Duff Moisture Code index                     | Float      |
| DC       | Drought Code index                           | Float      |
| ISI      | Initial Spread Index                         | Float      |
| temp     | Temperature in Celsius degrees               | Float      |
| RH       | Relative Humidity in %                       | Integer    |
| wind     | Wind speed in km/h                           | Float      |
| rain     | Outside rain in mm/m2                        | Float      |
| area     | The burned area of the forest (in ha)        | Float      |

## Objective
The primary objective is to construct and evaluate model pipelines capable of predicting the burned area of forest fires using the provided dataset. This involves:

- Building multiple model pipelines combining different preprocessors and regressors.
- Evaluating and tuning these models using appropriate performance metrics.
- Selecting the best-performing model based on evaluation results.

## Implementation Details

### Preprocessors
Two types of preprocessors are used:

1. **Preproc1**: Scales numeric variables and applies one-hot encoding to categorical variables.
2. **Preproc2**: Scales numeric variables, applies non-linear transformations, and one-hot encodes categorical variables.

### Regressors
Multiple regressor options are explored:

- Baseline models (e.g., K-nearest neighbors, Linear Regression)
- Advanced models (e.g., Random Forest, Neural Network)

### Model Evaluation
Models are evaluated using metrics such as RMSE, MAE, and R-squared to ensure robust performance measurement.

### Pipeline Construction
Pipelines are constructed combining each preprocessor with each type of regressor to examine their effectiveness.

## Usage

To replicate the analysis:

1. Ensure that the dataset is located as specified.
2. Run the provided Jupyter Notebook which includes detailed steps from data loading and preprocessing to model training and evaluation.

## Results
Detailed results of the model evaluations are presented in the notebook, highlighting the performance of each
