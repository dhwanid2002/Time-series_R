# Time-series_R
This code is a comprehensive demonstration of time series analysis and forecasting using R. It involves multiple steps, including visualization, decomposition, model building, and forecasting. Here's a breakdown of each code chunk:

### 1. **Initial Setup and Visualization:**
   - **Chunk 1:** Loads and plots the `USgas` dataset (monthly natural gas consumption in the US) using the `TSstudio` package.
   - **Chunk 2:** Displays basic information about the time series dataset.
   - **Chunk 3:** Decomposes the time series into trend, seasonal, and remainder components.

### 2. **Data Preparation for Forecasting:**
   - **Chunk 4-5:** Converts the `USgas` dataset to a format suitable for the `prophet` package and examines the first few rows.
   - **Chunk 6-8:** Adds a `trend` variable and a `seasonal` variable (month of year) for modeling.

### 3. **Data Splitting and Model Fitting:**
   - **Chunk 9:** Splits the data into training and testing sets for model validation.
   - **Chunk 10-12:** Builds and evaluates a linear model (`lm`) on the trend component.
   - **Chunk 13-14:** Visualizes and calculates the Mean Absolute Percentage Error (MAPE) for the trend model.
   - **Chunk 15-17:** Builds and evaluates a linear model on the seasonal component, visualizes the results, and calculates MAPE.
   - **Chunk 18-20:** Combines trend and seasonal components in a single model, evaluates, and calculates MAPE.
   - **Chunk 21-22:** Adds a quadratic term for the trend in the model and evaluates its performance.
   - **Chunk 23-24:** Splits the `USgas` dataset again and fits a time series linear model (`tslm`) with trend, seasonality, and quadratic terms.

### 4. **Break Point Analysis and New Dataset:**
   - **Chunk 25:** Introduces a step change (`s_break`) and fits an updated model.
   - **Chunk 26:** Loads and visualizes a new dataset (`UKdaily`), representing the UK's daily national demand for electricity.
   
### 5. **Exploratory Data Analysis:**
   - **Chunk 27-28:** Adds more features (weekday, month, lag variables) to the `UKdaily` dataset and creates a time series object.
   - **Chunk 29:** Splits the UK dataset and prepares training and testing subsets.

### 6. **Model Building and Forecasting for UK Dataset:**
   - **Chunk 30:** Fits a basic time series linear model to the UK data and makes predictions.
   - **Chunk 31-32:** Enhances the model by adding additional predictors (weekday, month, and lag) and evaluates the forecasting accuracy.
   - **Chunk 33-34:** Performs statistical tests (ANOVA) and checks model residuals.
   - **Chunk 35:** Finalizes the model with all variables, including seasonal, trend, weekday, month, and lag features.
   - **Chunk 36:** Assesses the residuals to ensure the model is well-fitted.

### 7. **Forecasting and Visualization for the UK Dataset:**
   - **Chunk 37-38:** Prepares future forecast data, including lag and calendar-related variables.
   - **Chunk 39:** Uses the final model to generate forecasts for the next year (365 days).
   - **Chunk 40:** Plots the forecasted electricity demand for the UK.

### Key Insights:
- This code demonstrates how to handle time series data, decompose it into components, and apply different models (e.g., linear models, time series models) for forecasting.
- It explores various model formulations, including trend, seasonality, and additional explanatory variables (such as weekday and month).
- It uses multiple forecasting techniques and evaluates model performance using metrics like MAPE and residual diagnostics.
