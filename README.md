# Forecasting Future Sales Using ARIMA and SARIMAX

This project demonstrates the application of time series analysis to forecast monthly champagne sales. It covers the end-to-end process of time series modeling, including data visualization, stationarity testing, differencing, and model evaluation using **ARIMA** (Autoregressive Integrated Moving Average) and **SARIMAX** (Seasonal ARIMA with eXogenous factors).

## Project Overview

The objective is to predict future sales for "Perrin Freres" monthly champagne sales using historical data from 1964 to 1972.

### Key Steps:
1.  **Visualize the Time Series Data:** Understand trends, cycles, and seasonality.
2.  **Stationarity Testing:** Using the Augmented Dickey-Fuller (ADF) test to check if the data is stationary.
3.  **Differencing:** Transforming non-stationary data into stationary data (First and Seasonal differencing).
4.  **Correlation Analysis:** Plotting ACF (Autocorrelation) and PACF (Partial Autocorrelation) charts to determine model parameters (p, d, q).
5.  **Model Building:** Constructing and training ARIMA and SARIMAX models.
6.  **Prediction:** Using the trained model to forecast and validate against actual data.

## Dataset

* **File:** `perrin-freres-monthly-champagne-.csv`
* **Columns:**
    * `Month`: Monthly time steps (converted to Datetime format).
    * `Sales`: Monthly champagne sales volume.

## Implementation Details

### Stationarity
The initial data was found to be non-stationary (p-value > 0.05). Seasonality was addressed using a 12-month seasonal shift, which successfully achieved stationarity.

### Models Used
* **ARIMA:** Used for general time series forecasting but struggled with the highly seasonal nature of the champagne data.
* **SARIMAX:** Optimized to handle the 12-month seasonality, resulting in significantly more accurate forecasts.

## Requirements

To run this project, you need the following Python libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `statsmodels`

## Usage

1.  Clone the repository.
2.  Ensure `perrin-freres-monthly-champagne-.csv` is in the project root.
3.  Open `Forecasting_Future_Sales_Using_ARIMA_and_SARIMAX.ipynb` in Jupyter Notebook or Google Colab.
4.  Run all cells to see the visualization, statistical tests, and final forecasting plots.

## Results & Visualizations
The project concludes by visualizing the predicted sales vs. the actual historical sales. As shown below, the SARIMAX model successfully captures the end-of-year peaks characteristic of champagne sales:

![SARIMAX Sales Forecast](<img width="1003" height="659" alt="sales_and_forecaste" src="https://github.com/user-attachments/assets/bc6e2776-4e1a-44aa-a6dc-49d3df182d47" />
)
