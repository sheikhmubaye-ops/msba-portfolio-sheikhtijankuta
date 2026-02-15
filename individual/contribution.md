Final version-strong interview style
I contributed primarily to feature engineering and model development. I worked on handling null values appropriately, creating engineered features such as referral thresholds and service counts, and testing multiple models. I also contributed to tuning the XGBoost model and evaluating performance using ROC-AUC
I advocated for using XGBoost as the final model due to its strong ability to handle nonlinear relationships and class imbalance. Given our dataset had significantly more non-churners than churners, XGBoost’s scale_pos_weight parameter allowed us to better account for imbalance while maintaining high predictive performance.
One key lesson was the importance of thoughtful feature engineering. Aggregating services and add-ons into counts provided clearer predictive signals than treating each service independently.

