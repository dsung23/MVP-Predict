# NBA MVP Prediction Model


Advanced data science project building a predictive model for NBA Most Valuable Player (MVP) voting. Analyzes 30+ years of NBA statistics to predict MVP vote shares using ensemble machine learning methods, achieving a Mean Average Precision (MAP) of 0.8096.

## 🎯 Key Features

- **Advanced Feature Engineering**: 50+ statistical predictors including traditional and advanced metrics
- **Machine Learning Pipeline**: Ensemble voting regressor (Random Forest, Gradient Boosting, Hist Gradient Boosting)
- **Performance Metrics**: Mean Average Precision (MAP) of 0.8096 for ranking accuracy

## 📊 Technical Stack

- **Python**: Pandas, NumPy, Scikit-learn
- **Web Scraping**: Automated data extraction from Basketball Reference
- **Machine Learning**: Ensemble methods (Voting Regressor with Random Forest, Gradient Boosting, Hist Gradient Boosting)
- **Advanced Analytics**: Player Efficiency Rating (PER), Win Shares, Box Plus/Minus, VORP

## 🔬 Methodology

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
- **Algorithm**: Ensemble Voting Regressor combining Random Forest, Gradient Boosting, and Hist Gradient Boosting
- **Training Strategy**: Time-based cross-validation (1996-2024) with rolling window approach
- **Evaluation**: Mean Average Precision (MAP) for ranking accuracy
- **Model Performance**: Achieved MAP of 0.8096 across 29 years of backtesting

## 📈 Key Results
### Top 5 MVP Predictions vs Actual Results for 2025

| Player | Predicted Vote Share | Actual Vote Share | Actual Rank | Predicted Rank | Rank Difference |
|--------|---------------------|-------------------|-------------|----------------|-----------------|
| Shai Gilgeous-Alexander | 0.933 | 0.913 | 1 | 1 | 0 |
| Nikola Jokić | 0.711 | 0.787 | 2 | 2 | 0 |
| Giannis Antetokounmpo | 0.357 | 0.470 | 3 | 3 | 0 |
| Trae Young | 0.161 | 0.000 | 11 | 4 | +7 |
| Jayson Tatum | 0.108 | 0.311 | 4 | 5 | -1 |

**Key Results:**
- **Perfect Top 3**: Model correctly predicted the top 3 MVP candidates in exact order
- **Top 3 Accuracy**: 100% (3/3 correct rankings)
- **Top 5 Accuracy**: 60% (3/5 correct rankings)
- **Average Rank Difference**: 1.6 positions
### Model Capabilities
- Successfully predicts MVP vote shares and player rankings with 80.96% accuracy
- Identifies key statistical factors influencing MVP voting
- Evaluates ranking accuracy using Mean Average Precision (MAP)
- Demonstrates strong performance in recent years (MAP of 0.8698 for 2010-2024)

### Technical Achievements
- **Data Scale**: 5.9MB comprehensive dataset with 30+ years of NBA history
- **Feature Complexity**: 50+ engineered features combining traditional and advanced metrics
- **Model Robustness**: Ensemble voting regressor improves accuracy and reduces overfitting
- **Advanced Evaluation**: MAP of 0.8096 with strong recent performance (0.8698 for 2010-2024)

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas scikit-learn jupyter tqdm
```

### Running the Project
Execute `machine_learning_v2.ipynb` for predictions

--
