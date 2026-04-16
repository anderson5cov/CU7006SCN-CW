# CU7006SCN-CW

project/
├── notebooks/
│   ├── 1_data_ingestion.ipynb
│   ├── 2_feature_engineering.ipynb
│   ├── 3_model_training.ipynb
│   ├── 4_evaluation.ipynb
│   └── 5_tableau_export.ipynb
├── tableau/
│   ├── kingdom_distribution.csv
│   ├── data_quality.csv
│   ├── records_over_time.csv
│   ├── model_performance.csv
│   ├── feature_importance.csv
│   ├── sklearn_vs_mllib.csv
│   ├── geographic_spread.csv
│   ├── specimen_types.csv
│   ├── scalability.csv
│   ├── training_times.csv
│   └── roc_curve.csv
├── config/
│   └── spark_config.yaml
└── README.md

# Technical Stack
- Platform: Databricks (Serverless Compute)
- Language: Python 3.12
- Framework: Apache PySpark
- ML Library: MLlib
- Visualisation: Tableau Public
- Storage Format: Parquet 

# How to Run
- Databricks workspace with serverless compute
- Dataset uploaded to `/Volumes/workspace/default/museum/`

# Steps
1. Run `1_data_ingestion.ipynb` — unzips and loads the dataset, saves as Parquet
2. Run `2_feature_engineering.ipynb` — cleans data, encodes features, saves prepared data
3. Run `3_model_training.ipynb` — trains all 4 models, runs CrossValidator, saves models
4. Run `4_evaluation.ipynb` — evaluates models, generates confusion matrices, ROC curve
5. Run `5_tableau_export.ipynb` — exports CSV files for Tableau dashboards

# Paths
- Raw data: `/Volumes/workspace/default/museum/unzipped/resource.csv`
- Parquet: `/Volumes/workspace/default/museum/parquet/`
- Prepared data: `/Volumes/workspace/default/museum/prepared/`
- Models: `/Volumes/workspace/default/museum/models/`
- Tableau exports: `/Volumes/workspace/default/museum/tableau/`
