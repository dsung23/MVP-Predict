# NBA MVP Prediction Model

Advanced data science project building a predictive model for NBA Most Valuable Player (MVP) voting. Analyzes 30+ years of NBA statistics to predict MVP vote shares using ensemble machine learning methods, achieving a Mean Average Precision (MAP) of 0.8127.

## Key Features

- **Advanced Feature Engineering**: 50+ statistical predictors including traditional and advanced metrics
- **Machine Learning Pipeline**: Ensemble Voting Regressor (Random Forest, Gradient Boosting, Hist Gradient Boosting)
- **Performance Metrics**: Mean Average Precision (MAP) of 0.8127 for ranking accuracy
- **Model Comparison**: HistGradientBoosting achieves MAP of 0.7914 in under 1 minute

## Technical Stack

- **Python**: Pandas, NumPy, Scikit-learn
- **Web Scraping**: Automated data extraction from Basketball Reference
- **Machine Learning**: Ensemble Voting Regressor with HistGradientBoosting as baseline
- **Advanced Analytics**: Player Efficiency Rating (PER), Win Shares, Box Plus/Minus, VORP

## Methodology

### Data Collection & Processing
- **Comprehensive Coverage**: 30+ years of NBA data (1991-2025)
- **Data Quality**: Missing value handling, outlier detection, validation
- **Feature Engineering**: Added relative performance ratios (PTS_T, AST_R, STL_R, BLK_R, 3P_R)

### Feature Engineering
The model incorporates 50+ predictive features:

**Traditional Statistics:** Points, Rebounds, Assists, Field Goal %, Games played
**Advanced Metrics:** Player Efficiency Rating (PER), Win Shares, Box Plus/Minus, VORP
**Team Performance:** Win/Loss record, offensive/defensive ratings
**Relative Performance:** Year-normalized ratios for points, assists, steals, blocks, 3-pointers

### Machine Learning Approach
- **Primary Algorithm**: Ensemble Voting Regressor combining Random Forest, Gradient Boosting, and Hist Gradient Boosting
- **Baseline Model**: HistGradientBoosting Regressor for quick demonstrations
- **Training Strategy**: Time-based cross-validation (1996-2025) with rolling window approach
- **Evaluation**: Mean Average Precision (MAP) for ranking accuracy
- **Model Performance**: Achieved MAP of 0.8127 across 30 years of backtesting

## Key Results
### Top 5 MVP Predictions vs Actual Results for 2025

| Player | Predicted Vote Share | Actual Vote Share | Actual Rank | Predicted Rank | Rank Difference |
|--------|---------------------|-------------------|-------------|----------------|-----------------|
| Shai Gilgeous-Alexander | 0.794 | 0.913 | 1 | 1 | 0 |
| Nikola Jokić | 0.571 | 0.787 | 2 | 2 | 0 |
| Giannis Antetokounmpo | 0.305 | 0.470 | 3 | 3 | 0 |
| Jayson Tatum | 0.084 | 0.311 | 4 | 4 | 0 |
| Trae Young | 0.071 | 0.000 | 11 | 5 | +6 |

### Model Capabilities
- Successfully predicts MVP vote shares and player rankings with 81.27% accuracy
- Evaluates ranking accuracy using Mean Average Precision (MAP)
- Demonstrates strong performance in recent years (MAP of 0.8965 for 2019-2025)

### Technical Achievements
- **Data Scale**: 16,033 player seasons across 30+ years of NBA history
- **Feature Complexity**: 50+ engineered features combining traditional and advanced metrics
- **Model Robustness**: Ensemble voting regressor improves accuracy and reduces overfitting
- **Advanced Evaluation**: MAP of 0.8127 with strong recent performance (0.8965 for 2019-2025)

## Getting Started

### Prerequisites
```bash
pip install pandas scikit-learn jupyter tqdm 
```

### Running the Project
Execute `machine_learning_v2.ipynb` for predictions

**Note**: The notebook includes both individual models and an ensemble approach. 
The HistGradientBoosting model provides excellent performance (MAP: 0.7914) around 3
 minutes for quick demonstrations. The ensemble Voting Regressor 
achieves slightly higher accuracy (MAP: 0.8127) and also takes around 3 minutes.

## Model Performance Over Time

The model demonstrates consistent performance across different eras:
- **Overall Performance (1996-2025)**: MAP of 0.8127
- **Recent Performance (2019-2025)**: MAP of 0.8965 (+10.3% improvement)
- **Peak Performance**: 2003 season achieved perfect 1.000 MAP
- **Most Challenging**: 2005 season with 0.4208 MAP

## Key Insights

- **Perfect Top 3 Prediction**: Model correctly predicted the top 4 MVP finishers for 2025 in correct order
- **Ranking Accuracy**: Successfully identifies MVP candidates with high precision
- **Feature Importance**: Advanced metrics (PER, Win Shares, VORP) are crucial predictors
- **Team Performance**: Team winning percentage significantly influences MVP voting patterns
