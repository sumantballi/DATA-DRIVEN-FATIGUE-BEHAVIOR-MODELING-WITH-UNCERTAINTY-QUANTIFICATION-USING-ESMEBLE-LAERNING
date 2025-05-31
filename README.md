# DATA-DRIVEN-FATIGUE-BEHAVIOR-MODELING-WITH-UNCERTAINTY-QUANTIFICATION-USING-ESMEBLE-LAERNING

**INTRODUCTION**

Fatigue analysis is a crucial aspect of structural health and component longevity. In this study, we explore the use of ensemble-based regression models to predict fatigue-related mechanical responses and quantify uncertainty in the predictions. We evaluate three different data-splitting strategies:

Cross-Validation

Train-Test Split

Train-Validation-Test Split

We use metrics including Pearson Correlation Coefficient (CC), R² Score, RMSE, MAE, Prediction Interval Coverage Probability (PICP), Median Prediction Interval Width (MPIW), and a Composite Metric to compare the robustness of each method.

**METHODOLOGY**

Model and Uncertainty Estimation

We used an ensemble of regressors with predictive intervals, specifically focusing on quantile-based uncertainty calibration. The ensemble is built using GradientBoostingRegressor with tuned hyperparameters for maximum depth and number of estimators.

EVALUATION METRICS

Pearson CC: Measures linear correlation.

R² Score: Indicates goodness of fit.

RMSE/MAE: Root Mean Square Error and Mean Absolute Error, reflecting average prediction error.

Coverage (%): Percentage of targets falling within the predictive intervals.

Interval Width: Represents the spread or uncertainty range.

Composite Metric: A balanced score combining performance and uncertainty metrics.

**EXPERIMENTAL SETUP**

DATA PREPROCESSING

Features were standardized.

The target variable was normalized (if applicable).

Outliers were retained to ensure generalization capability.

APPROACH SUMMARY

Approach

Splits Used

Tuning Done

Fatigue_Analysis_Cross_Validation

5-Fold Cross-Validation (nruns=1)

No tuning, just performance spread

Fatigue_Analysis_Test_Train

80% Train / 20% Test

No separate validation

Fatigue_Analysis_Train_Val_Test

70% Train / 15% Val / 15% Test

Hyperparameter tuning on validation

**RESULT AND ANALYSIS**

Performance Metrics by Approach

Approach

Composite Metric (Test)

Interval Width

Coverage (%)

Generalization

Cross-Validation (avg)

0.855

1.358 (avg)

89.5 (avg)

Robust but no tuning

Test-Train Split

0.827

1.539

88.64

Single split, no tuning

Train-Val-Test

0.939

0.972

90.9

Tuned, most reliable

Key Insights

The Train-Validation-Test split approach yields the best overall performance, thanks to targeted hyperparameter tuning. It balances prediction accuracy with tight, well-calibrated uncertainty estimates, making it the recommended strategy for real-world deployment.

**CONCLUSION**

This study demonstrates that ensemble models with calibrated predictive intervals can achieve high accuracy in fatigue analysis. Among the evaluated approaches, the Train-Validation-Test strategy outperforms others in both predictive performance and uncertainty quantification. This highlights the importance of proper model validation and tuning when applying machine learning to critical engineering domains like fatigue behavior modeling.

**REFERENCES**

## 📚 References

1. Chang, J., Basvoju, D., Vakanski, A., Charit, I., & Xian, M. (2025). *Predictive Modeling and Uncertainty Quantification of Fatigue Life in Metal Alloys using Machine Learning*. arXiv preprint [arXiv:2501.15057](https://arxiv.org/abs/2501.15057)

2. Swetlana, S., Rout, A., & Singh, A. K. (2023). *Machine learning assisted interpretation of creep and fatigue life in titanium alloys*. [Materials Today: Proceedings](https://doi.org/10.1016/j.matpr.2023.11.117) *(Open Access)*


