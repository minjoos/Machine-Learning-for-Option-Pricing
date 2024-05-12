# Results Summary

## Project Overview
This project evaluates the effectiveness of various machine learning models over the traditional Black-Scholes model in predicting the prices of European call options on the S&P 500. Our analysis explored both regression and classification models to predict option values and assess the accuracy of predictions relative to actual market prices.

## Data
The analysis utilized a dataset named `option_train.csv`, consisting of European call options with features like current asset value (S), strike price (K), time to maturity (tau), and risk-free interest rate (r). The dataset includes responses for actual option values and their corresponding Black-Scholes model values.

## Models Evaluated
We conducted our analysis using the following models:
- Linear Regression
- K-Nearest Neighbors (KNN)
- Decision Trees
- Random Forest
- Gradient Boosting
- XGBoosting

## Regression Analysis Results
The regression models aimed to predict the actual value of the options. Our findings are summarized in the table below:

| Model               | Out-of-Sample R² | RMSE   |
|---------------------|------------------|--------|
| Linear Regression   | 0.924            | 34.30  |
| KNN                 | 0.947            | 28.38  |
| Decision Tree       | 0.991            | 11.43  |
| Random Forest       | 0.996            | 7.66   |
| **Gradient Boosting** | **0.997**        | **6.62**  |
| XGBoosting          | 0.983            | 16.10  |

Gradient Boosting emerged as the superior model with the highest R² and the lowest RMSE, indicating its robustness and accuracy in handling complex option pricing scenarios.

## Classification Analysis Results
The classification models evaluated the accuracy of the option value predictions against the Black-Scholes model values, converted into binary classifications of over or under predictions:

| Model               | Classification Error | Confusion Matrix        |
|---------------------|----------------------|-------------------------|
| Logistic Regression | 0.109                | [[1109, 65], [100, 226]]|
| KNN                 | 0.089                | [[1094, 80], [55, 271]] |
| Decision Tree       | 0.086                | [[1095, 79], [50, 276]] |
| Random Forest       | 0.078                | [[1120, 54], [63, 263]] |
| **Gradient Boosting** | **0.067**            | **[[1125, 49], [52, 274]]** |
| XGBoosting          | 0.067                | [[1118, 56], [47, 279]] |

Again, Gradient Boosting demonstrated the lowest classification error, showcasing its efficiency in predicting pricing errors more accurately than other models.

## Conclusion
The Gradient Boosting model stood out as the most effective in both regression and classification tasks. Its ability to handle non-linear relationships and complex dataset structures makes it particularly valuable for financial applications like option pricing.

For more detailed insights and a comprehensive discussion of the methodology, please refer to our full project report available in the repository: [Options Pricing Analysis Report](options_pricing_analysis_report.pdf).
