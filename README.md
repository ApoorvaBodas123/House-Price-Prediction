# House Price Prediction - King County, USA

A machine learning project that predicts house prices in King County, Washington (including Seattle) using linear regression.

## 📊 Dataset

This project uses the **House Sales in King County, USA** dataset from Kaggle:
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
- **Time Period**: May 2014 - May 2015
- **Records**: 21,613 house sales
- **License**: CC0: Public Domain

### Dataset Features

The dataset contains 21 features including:

| Feature | Description | Type |
|---------|-------------|------|
| `price` | Sale price (target variable) | Float |
| `bedrooms` | Number of bedrooms | Integer |
| `bathrooms` | Number of bathrooms | Float |
| `sqft_living` | Living area square footage | Integer |
| `sqft_lot` | Lot square footage | Integer |
| `floors` | Number of floors | Float |
| `waterfront` | Waterfront property (0/1) | Integer |
| `view` | View quality (0-4) | Integer |
| `condition` | Overall condition (1-5) | Integer |
| `grade` | Construction grade (1-13) | Integer |
| `sqft_above` | Above ground square footage | Integer |
| `sqft_basement` | Basement square footage | Integer |
| `yr_built` | Year built | Integer |
| `yr_renovated` | Year renovated (0 if never) | Integer |
| `zipcode` | ZIP code | Integer |
| `lat` | Latitude | Float |
| `long` | Longitude | Float |
| `sqft_living15` | Living area of 15 nearest neighbors | Integer |
| `sqft_lot15` | Lot area of 15 nearest neighbors | Integer |

## 🛠️ Project Structure

```
House-Price-Prediction/
├── README.md                    # This file
├── house_price_prediction.ipynb # Main Jupyter notebook
├── kc_house_data.csv           # Dataset (gitignored)
└── .gitignore                  # Git ignore file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required packages:
  - pandas
  - numpy
  - matplotlib
  - scikit-learn

### Installation

```bash
pip install pandas numpy matplotlib scikit-learn jupyter
```

### Running the Project

1. Clone this repository
2. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/harlfoxem/housesalesprediction)
3. Place `kc_house_data.csv` in the project directory
4. Open and run the Jupyter notebook:

```bash
jupyter notebook house_price_prediction.ipynb
```

## 📈 Model Performance

The current implementation uses **Linear Regression** with the following metrics:

- **Mean Absolute Error (MAE)**: $127,711.87
- **Mean Squared Error (MSE)**: 48,213,882,976.97
- **Root Mean Squared Error (RMSE)**: $219,576.60
- **R² Score**: 0.686 (68.6% variance explained)

## 🔬 Methodology

### Data Preprocessing
- **Missing Values**: No missing values found in the dataset
- **Feature Selection**: Removed `id`, `date`, and target variable `price` from features
- **Train-Test Split**: 80% training, 20% testing (random_state=12)

### Model Training
- **Algorithm**: Linear Regression
- **Features**: 18 predictive features
- **Target**: House price

### Evaluation
- Comprehensive error metrics calculated
- Visualization of actual vs predicted prices
- Model explains approximately 68.6% of price variance

## 📊 Key Insights

### Dataset Statistics
- **Average House Price**: $540,081
- **Price Range**: $75,000 - $7,700,000
- **Average Living Area**: 2,080 sq ft
- **Average Year Built**: 1971
- **Most Common**: 3 bedrooms, 2.25 bathrooms

### Model Performance
- The model achieves moderate performance with R² = 0.686
- Prediction errors are significant, suggesting room for improvement
- Linear regression may be too simple for this complex relationship

## 🔮 Future Improvements

1. **Feature Engineering**
   - Create age-related features (years since built/renovated)
   - Extract meaningful features from date
   - Create location-based features from lat/long

2. **Advanced Models**
   - Try Random Forest, Gradient Boosting, or XGBoost
   - Implement neural networks for non-linear relationships
   - Use ensemble methods

3. **Hyperparameter Tuning**
   - Grid search or random search for optimal parameters
   - Cross-validation for robust evaluation

4. **Feature Selection**
   - Use recursive feature elimination
   - Apply regularization techniques (Lasso, Ridge)
   - Feature importance analysis

## 📝 Notebook Contents

The `house_price_prediction.ipynb` notebook includes:

1. **Data Loading & Exploration**
   - Import libraries
   - Load and inspect dataset
   - Basic statistics and info

2. **Data Preprocessing**
   - Check for missing values
   - Feature-target separation
   - Train-test split

3. **Model Training**
   - Linear Regression implementation
   - Model fitting

4. **Evaluation**
   - Calculate performance metrics
   - Visualize predictions vs actual values
   - Results analysis

## 📄 License

This project is open source and available under the MIT License. The dataset is licensed under CC0: Public Domain.

**Note**: Make sure to download the dataset from Kaggle and place it in the project directory before running the notebook.