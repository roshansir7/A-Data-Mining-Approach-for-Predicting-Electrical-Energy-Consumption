# Predicting Electrical Energy Consumption

A machine-learning project that explores electrical and weather data to predict **active power consumption**.

## Research Aim

The project investigates whether environmental conditions and electrical measurements can be used to estimate electricity usage accurately.

Reliable consumption prediction can support:

* Energy-demand planning
* Efficient power management
* Identification of consumption patterns
* Reduction of energy waste
* Improved operational decision-making

## Data Used

The dataset combines electrical measurements with weather information recorded over time.

### Electrical Variables

* Active power
* Current
* Voltage
* Reactive power
* Apparent power
* Power factor

### Weather Variables

* Temperature
* Feels-like temperature
* Minimum and maximum temperature
* Atmospheric pressure
* Humidity
* Wind speed
* Wind direction
* Weather condition and description

The prediction target is:

```text
active_power
```

## Project Pipeline

```text
Raw Energy and Weather Data
            |
            v
Data Inspection and Cleaning
            |
            v
Exploratory Data Analysis
            |
            v
Feature Preparation and Scaling
            |
            v
Time-Based Training and Testing
            |
            v
Regression Model Comparison
            |
            v
Energy Consumption Predictions
```

## Exploratory Analysis

The notebook examines:

* The distribution of active power consumption
* Relationships between electrical variables
* Connections between weather and energy usage
* Correlations among numerical features
* Outliers and unusual consumption values
* Changes in energy demand over time

The analysis shows that electrical measurements such as current and apparent power are important predictors of active power.

## Models Evaluated

Four regression algorithms are used:

| Model             | Role                                           |
| ----------------- | ---------------------------------------------- |
| Linear Regression | Interpretable baseline model                   |
| Decision Tree     | Captures nonlinear relationships               |
| Random Forest     | Ensemble model for improved stability          |
| XGBoost           | Boosting model for complex prediction patterns |

## Model Evaluation

The models are evaluated using:

* Mean Absolute Error
* Mean Squared Error
* Root Mean Squared Error
* R-squared score
* Actual-versus-predicted comparisons

Time-based validation is used to reduce the risk of using future observations to predict earlier records.

## Model Optimisation

The project uses techniques such as:

* Standardisation of numerical features
* Time-series cross-validation
* Randomised hyperparameter search
* Model comparison
* Feature-importance analysis

These steps help identify the most reliable model and the variables that contribute most strongly to energy prediction.

## Technologies

```text
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
XGBoost
Google Colab
Jupyter Notebook
```

## Repository File

```text
Data_Mining_code.ipynb
```

The notebook contains the complete workflow, including data loading, cleaning, exploratory analysis, model training, optimisation, evaluation, and visualisation.

## Running the Project

Clone the repository:

```bash
git clone https://github.com/roshansir7/A-Data-Mining-Approach-for-Predicting-Electrical-Energy-Consumption.git
```

Open the project directory:

```bash
cd A-Data-Mining-Approach-for-Predicting-Electrical-Energy-Consumption
```

Start Jupyter Notebook:

```bash
jupyter notebook Data_Mining_code.ipynb
```

Place the following dataset in the expected location before running the notebook:

```text
energy_weather_raw_data.csv
```

You may need to update the dataset path in the notebook when running it outside Google Colab.

## Project Outcome

This project demonstrates how data-mining and regression techniques can be applied to electricity-consumption forecasting.

It provides experience in:

* Working with large time-based datasets
* Combining weather and electrical information
* Performing exploratory data analysis
* Developing regression models
* Tuning machine-learning algorithms
* Comparing prediction performance
* Translating model results into energy-management insights

## Limitations

* The dataset is not currently included in the repository.
* Results depend on the location and period represented by the data.
* Closely related electrical variables may introduce data leakage when predicting active power.
* Additional testing on unseen time periods would improve confidence in model generalisation.
* The notebook is designed for experimentation rather than production deployment.
