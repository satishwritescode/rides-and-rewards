# NYC Yellow Taxi Fare Prediction Project

## Overview
This repository contains the code and documentation for the Final Group Project (Spring 2024) by Team 10. The project focuses on predicting the total fare of yellow taxi trips in New York City using comprehensive trip data. The analysis includes data preparation, exploratory data analysis (EDA), feature engineering, and modeling to identify key factors influencing fare variability.

## Research Question
How can we effectively predict the total fare of yellow taxi trips in New York City using available trip data, and what factors most significantly contribute to the variability in fares charged to passengers?

## Dataset
The project utilizes two primary datasets:
1. **taxi_zone_lookup.csv**: Contains geographical details of taxi zones in NYC.
2. **yellow_tripdata_2024-01.parquet**: Contains detailed trip records for yellow taxis in NYC for January 2024, including variables such as trip distance, fare amount, passenger count, and various surcharges.

These datasets are publicly available from the NYC Taxi and Limousine Commission (TLC).

## Project Structure
- **Data Science Project Spring 2024.Rmd**: The main R Markdown file containing the complete analysis, including:
  - Data loading and preprocessing
  - Feature engineering
  - Model development (GLM and Ridge Regression)
  - Model diagnostics
  - Exploratory data analysis (EDA) with visualizations
  - Results and predictions
- **README.md**: This file, providing an overview of the project and instructions for use.

## Prerequisites
To run the code in this repository, you need the following R packages installed:
- `arrow`
- `lubridate`
- `caret`
- `dplyr`
- `randomForest`
- `ggplot2`
- `sf`
- `readr`
- `boot`
- `glmnet`
- `Metrics`
- `pROC`

You can install these packages in R using:
```R
install.packages(c("arrow", "lubridate", "caret", "dplyr", "randomForest", "ggplot2", "sf", "readr", "boot", "glmnet", "Metrics", "pROC"))
```

## Usage
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/nyc-taxi-fare-prediction.git
   ```
2. **Download the Datasets**:
   - Obtain `taxi_zone_lookup.csv` and `yellow_tripdata_2024-01.parquet` from the [NYC TLC Trip Record Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page).
   - Place the datasets in the appropriate directory and update the file paths in the R Markdown file if necessary.
3. **Run the Analysis**:
   - Open `Data Science Project Spring 2024.Rmd` in RStudio.
   - Ensure all required packages are installed.
   - Knit the R Markdown file to generate the analysis report in PDF format.

## Methodology
- **Data Preparation**: The data is cleaned and preprocessed to focus on credit card transactions, with derived features such as trip duration, pickup/drop-off hours, and weekend indicators.
- **Feature Engineering**: Additional features like `added_fees_ratio` and `daytime_PU/DO` are created to enhance model performance.
- **Modeling**:
  - A Generalized Linear Model (GLM) is used to predict tip amounts based on various predictors.
  - Ridge Regression with cross-validation is applied to improve model robustness.
- **EDA**: Visualizations explore relationships between tip amounts, fare charged, trip distance, pickup/drop-off locations, and time of day.
- **Evaluation**: Models are evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), R-squared, and AUC.

## Key Findings
- Key predictors of taxi fares include trip distance, fare amount, and additional fees (e.g., congestion surcharge, airport fee).
- Pickup and drop-off locations, time of day, and whether the trip occurs on a weekend significantly influence fare variability.
- The Ridge Regression model with cross-validation provides improved predictive performance compared to the initial GLM model.

## Visualizations
The project includes several visualizations:
- Bar plots of pickup and drop-off location frequencies.
- Plots of average tip amounts by location, time of day, and passenger count.
- Scatter plots with regression lines showing relationships between tip amounts, fare charged, and trip distance.

## Future Work
- Incorporate additional months of data to capture seasonal trends.
- Explore other machine learning models (e.g., Random Forest, Gradient Boosting) for improved accuracy.
- Include spatial analysis using geographical coordinates from the taxi zone data.

## Contributors
- Team 10 (Spring 2024 Data Science Course)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact
For questions or feedback, please contact Team 10 via the repository's issues page.