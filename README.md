# StockData

## Overview

This repository contains various raw datasets that feature historical stock prices for different equities, recorded at a frequency of 1 minute. These datasets cover both market hours and after-hours trading. Additionally, you'll find a script detailing the preprocessing steps using the TESLA stock as an example. The preprocessed dataset is also available for direct download.

## Directory Structure
`datasets/raw/`: Contains the raw datasets, which are unprocessed.  
`datasets/processed/`: Contains the processed datasets, after cleaning, stock split adjustments, and other transformations.  
`notebooks/`: Jupyter notebooks that detail the preprocessing and analysis steps.  
`scripts/`: Python scripts, including ones for integrating stock price data with news datasets.    

## Preprocessing Details

The preprocessing steps for the stock data are demonstrated in the Jupyter notebook `TeslaStockDataPreprocessing.ipynb` within the `notebooks/` directory. The key steps include:

1. **Handling Missing Data**: Rows containing NaN values were identified and removed. Additionally, any duplicate rows were detected and one of them was dropped.
  
2. **Time Adjustments**: Adjustments were made for Daylight Saving Time. 

3. **Stock Split Adjustments**: Prices were adjusted for stock splits. For instance, TESLA's stock splits on specific dates have been taken into account.

4. **Market Hours**: The dataset was filtered to only include data from the market hours, which, due to the UTC0 timezone, corresponds to 14:30 to 21:00.

Feel free to explore the notebook for a more in-depth understanding and visualization of each step.
