# Biomass Forecasting In Gujarat

## Project Overview

This Jupyter Notebook project focuses on forecasting biomass availability in Gujarat using advanced machine learning algorithms. The objective is to enhance the accuracy of biomass predictions to support waste-to-energy projects and promote sustainable energy practices.

## Problem Statement

Biomass, derived from organic matter such as plants and animals, is a renewable energy source with significant potential for reducing reliance on fossil fuels and mitigating climate change. In Gujarat, where waste-to-energy projects are increasingly being implemented, accurate forecasting of biomass availability is critical for effective resource allocation and operational planning.

Traditional forecasting methods, such as linear regression and basic time series models, often fall short in capturing the complex relationships among various factors influencing biomass availability. These methods may not account for the intricate interplay of climatic variables, policy dynamics, precipitation patterns, and supply chain intricacies, leading to unreliable predictions.

To address these limitations, this project utilizes advanced machine learning algorithms, including Extra Trees Regressor (ETR), AdaBoost, Random Forest, Gradient Boosting, and Huber Regression. These algorithms leverage historical data and environmental variables to model complex biomass dynamics and provide more accurate forecasts.

Accurate biomass availability forecasts are essential for optimizing resource allocation, improving operational strategies, and informing policy decisions in waste-to-energy projects. By developing and validating predictive models with these advanced techniques, this project aims to bridge the gap between biomass forecasting and the needs of Gujarat's waste-to-energy sector, ultimately contributing to environmental sustainability and renewable energy adoption.

## Dataset

The dataset contains detailed information on biomass availability across various locations in Gujarat from 2010 to 2017. It includes:

- **Location Identifier**: Unique ID for each location.
- **Geographic Coordinates**: Latitude and longitude values.
- **Annual Biomass Records**: Columns for each year from 2010 to 2017.

### Sample Table of Dataset

| Index | Latitude | Longitude | 2010 | 2011 | 2012 | 2013 | 2014 | 2015 | 2016 | 2017 |
|-------------|----------|-----------|------|------|------|------|------|------|------|------|
| 001         | 23.0225  | 72.5714   | 500  | 520  | 540  | 560  | 580  | 600  | 620  | 640  |
| 002         | 22.3039  | 70.8022   | 300  | 320  | 340  | 360  | 380  | 400  | 420  | 440  |
| 003         | 21.1702  | 72.8311   | 450  | 470  | 490  | 510  | 530  | 550  | 570  | 590  |


## Implementation

### Hardware and Software

- **Hardware**: The notebook can be run on a Windows 10 machine with an Intel i5 processor and 8GB of RAM. GPU acceleration is not required but recommended for deep learning models.
- **Software**: The project uses Python along with libraries including `pandas`, `NumPy`, `scikit-learn`, and `shapely`.

### Results Calculation Formula

The accuracy of the forecasting models is evaluated using the Mean Absolute Error (MAE). The MAE is calculated as follows:

```python
MAE = np.mean(np.abs(forecast[year] - true[year]))
```
1. `forecast[year]` represents the predicted biomass values for a specific year.
2. `true[year]` represents the actual observed biomass values for the same year.
3. `np.mean` computes the average of the absolute differences between predicted and actual values.

## Dependencies

The following Python libraries are required for this project:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `shapely`
- `jupyter` (for running the notebook)

## Installation

To install the dependencies, you can use the following command:

```python
pip install numpy pandas matplotlib scikit-learn shapely jupyter
```

## Results

### Forecasting MAE

The performance of various machine learning models was evaluated based on the Mean Absolute Error (MAE) for the years 2018 and 2019. The results are summarized in the table below:

| Model Name                | MAE (2018) | MAE (2019) |
|---------------------------|------------|------------|
| Extra Tree Regressor      | 32.62      | 43.82      |
| Random Forest Regressor   | 31.11      | 45.39      |
| Ada Boost Regressor       | 41.72      | 47.03      |
| Gradient Boosting Regressor | 42.22    | 63.08      |
| Huber Regressor           | 57.76      | 89.92      |

- **Extra Tree Regressor (ETR)**: Demonstrated the best performance with the lowest MAE for both 2018 and 2019, making it the most effective model for forecasting biomass availability in this study.
- **Random Forest Regressor**: Followed closely behind ETR, indicating strong predictive capabilities.
- **Ada Boost Regressor**: Showed moderate performance, with higher MAE compared to ETR and Random Forest.
- **Gradient Boosting Regressor**: Had relatively high MAE values, particularly for 2019.
- **Huber Regressor**: Exhibited the highest MAE, suggesting less accuracy in predicting biomass availability.

## Conclusion

The study successfully applied advanced machine learning algorithms to forecast biomass availability in Gujarat. The Extra Tree Regressor emerged as the most accurate model, providing reliable predictions with the lowest MAE values. This indicates its potential for practical application in resource planning and decision-making for waste-to-energy projects.

The findings underscore the importance of utilizing sophisticated algorithms to enhance the accuracy of biomass forecasts. Accurate predictions are crucial for optimizing resource allocation and operational strategies, contributing to the efficiency and sustainability of biomass utilization in Gujarat's waste-to-energy sector.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request with your changes.

For more details, please refer to the documentation and the project repository.
