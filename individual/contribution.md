# Individual Contribution – Sheikh Tijan Kuta

## What I Contributed Most To

I contributed most to feature engineering and model evaluation.  
I helped design aggregated features such as number_of_services, number_of_addons, and referral flags to improve predictive power and business interpretability. I also focused on evaluating model performance using ROC-AUC and ensuring we properly handled class imbalance.

## One Decision I Personally Advocated For

I advocated for using XGBoost instead of relying only on logistic regression.  
My reasoning was that churn behavior is often nonlinear and influenced by interactions between contract type, tenure, and service usage. XGBoost allowed us to model these interactions while also handling class imbalance using scale_pos_weight.

## Lessons Learned & What I Would Improve

One key lesson was the importance of early-tenure customers as a high-risk segment. If we had more time, I would:

- Conduct a more structured A/B test simulation for retention incentives  
- Explore probability calibration to ensure predicted churn risk aligns with real-world percentages  
- Perform cost-benefit modeling to estimate ROI of retention offers  

