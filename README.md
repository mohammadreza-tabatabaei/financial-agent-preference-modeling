# Financial Agent Preference Prediction - ML Solution

## 📊 Project Overview
A comprehensive machine learning solution for **pairwise preference prediction** between trading agents using multivariate time-series financial data. This project demonstrates advanced feature engineering and ensemble modeling to determine superior trading performance based on OHLCV data and position sequences.

## 🎯 Business Problem
Predict which of two trading agents performs better given their historical:
- **Market Data**: OHLCV (Open, High, Low, Close, Volume)
- **Position Data**: Binary position masks indicating holding periods
- **Trading Behavior**: Entry/exit timing, risk management patterns

## 🏆 Technical Achievements
- **Cross-Validation Accuracy**: 78.31% (10-Fold Stratified)
- **Public Leaderboard Score**: 80.0%
- **Best Individual Model**: LightGBM (79.76% accuracy)
- **Ensemble Advantage**: +1.35% over best base model
- **Prediction Distribution**: 114 Agent A wins (54.8%), 94 Agent B wins (45.2%)

## 🔧 Technical Approach

### Feature Engineering (86 Features)
**Performance Metrics:**
- Multi-timeframe returns (total, short-term, medium-term)
- Risk-adjusted performance indicators (Sharpe ratio, profit factor)
- Momentum and trend strength analysis

**Trading Behavior Analysis:**
- Position timing efficiency and holding patterns
- Trading frequency and consistency metrics
- Win rate analysis and maximum drawdown

**Comparative Features:**
- Relative advantages between Agent A vs B
- Composite scoring systems
- Interaction metrics highlighting performance gaps

### Model Architecture
**Stacking Ensemble Framework:**
- **Base Models**: XGBoost, LightGBM, Random Forest, Gradient Boosting
- **Meta-Learner**: Logistic Regression with L2 regularization
- **Validation**: 10-Fold Stratified Cross-Validation
- **Feature Selection**: 30 most important features selected

### Data Preprocessing
- Robust scaling for financial data resilience
- Power transformation for distribution normalization
- Comprehensive missing value handling

## 📈 Key Insights Discovered
**Most Influential Factors:**
1. **Position Timing**: Entry/exit efficiency significantly impacts performance
2. **Risk Management**: Risk-adjusted returns more important than raw returns
3. **Trading Consistency**: Steady performance beats sporadic high returns
4. **Win Rate Quality**: Not just frequency, but magnitude and timing matter

**Behavioral Patterns:**
- Successful agents show optimal holding periods
- Consistent position switching correlates with lower performance
- Risk-aware strategies outperform aggressive approaches

## 🚀 Innovation & Methodology
**Advanced Analytical Techniques:**
- Trade reconstruction from binary position masks
- Composite multi-dimensional agent evaluation
- Robust validation with limited data
- Domain-driven interpretable features

**Technical Innovations:**
- Ensemble diversity optimization
- Feature importance-driven selection
- Production-ready preprocessing pipeline

## 🛠️ Installation & Usage
**Prerequisites:**
```bash
Python 3.8+
pip install -r requirements.txt
Key Dependencies:

python
pandas, numpy, scikit-learn
xgboost, lightgbm
matplotlib, seaborn
Run Analysis:

bash
jupyter notebook analysis_notebook.ipynb
💡 Business Applications
Algorithmic Trading Evaluation: Objective assessment of trading strategies

Risk Management Analysis: Understanding risk-taking behavior

Performance Benchmarking: Comparative analysis of trading agents

Strategy Optimization: Identifying successful approach characteristics

🔮 Future Enhancements
Technical Improvements:

Deep learning approaches (LSTMs, Transformers)

Market regime detection integration

Advanced position sizing analysis

Real-time adaptation capabilities

Feature Expansions:

Correlation analysis between agent behaviors

Advanced technical indicators

Portfolio-level performance metrics

👨‍💻 Author
Mohammadreza Tabatabaei
AI & Machine Learning Engineer with expertise in financial ML, time-series analysis, and production AI systems.

📄 License
This project is intended for portfolio demonstration purposes.
