# Track 3 – Deployment & Real-World Usage Plan

## Do predictions need to be instant?

Overnight batch scoring is sufficient.  
Customer churn risk does not change minute-by-minute, so daily or weekly scoring would provide enough timeliness while reducing infrastructure cost.

## How would predictions run and where would results be saved?

The model would run on a weekly schedule using a Python batch job.  
Predictions would be saved into a database table such as:

customer_churn_scores
- customer_id
- churn_probability
- score_date

This table could feed into a dashboard or CRM system for retention teams.

## Software Approach

A scheduled Python process using:

- SQL for data extraction
- Python for preprocessing and scoring
- A scheduler such as Airflow or a simple cron job

For more advanced implementation, FastAPI could expose the model as an internal API.

## Monitoring Plan

Data Quality Check:
- Monitor missing values and row counts daily to ensure data pipeline consistency.

Input Drift Check:
- Track distribution of key variables such as tenure and monthly_charge to detect changes.

Outcome Check:
- Monitor actual churn rate vs predicted churn rate (calibration tracking).
- Recalculate ROC-AUC quarterly to confirm model performance stability.
