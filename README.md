# Amsterdam Housing Price Analysis

Finall pushing this very old (2022) project analyzing Amsterdam housing market to github

## Overview

This project analyzes Amsterdam housing market data to:
- Understand price distributions and key factors affecting property values
- Map postal codes to Amsterdam districts for geographic analysis
- Build regression models to predict fair market prices
- Identify potentially underpriced properties based on model residuals

## Key Findings

- **Model Performance**: Ridge Regression achieved an RMSE of ~0.196 on log-transformed prices
- **Top Price Predictors**: Living area, number of rooms, bedrooms, and bathrooms are the strongest predictors
- **District Impact**: Canal Belt and Oud-Zuid command premium prices; Amsterdam Noord and ZuidOost are more affordable

## Dataset

The dataset contains ~2,000 Amsterdam property listings with features including:
- Price and price per m²
- Living area, bedrooms, bathrooms
- Building type (new/resale)
- House type (apartment/house)
- Energy label, balcony, garden
- Postal code and year built

**Source**: [Amsterdam Housing Data on Kaggle](https://www.kaggle.com/datasets)

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/GaloisTheory/amsterdam-housing-analysis.git
   cd amsterdam-housing-analysis
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook:
   ```bash
   jupyter notebook amsterdam-house-data-analysis.ipynb
   ```

## Methodology

1. **Data Exploration**: Distribution analysis, correlation heatmaps, box plots by category
2. **Feature Engineering**: 
   - Postal code → District mapping
   - Energy label encoding (A+ to G → 1 to 8)
   - House age calculation from year built
3. **Preprocessing**: Log transformation of skewed features, one-hot encoding of categoricals
4. **Modeling**: Linear Regression and Ridge Regression with cross-validation
5. **Analysis**: Residual analysis to find over/underpriced properties

## Project Structure

```
├── README.md
├── requirements.txt
├── amsterdam-house-data-analysis.ipynb   # Main analysis notebook
└── house_data4.csv                       # Housing dataset
```

## License

This project is for educational purposes.

