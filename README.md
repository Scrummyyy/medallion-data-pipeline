# medallion-data-pipeline
Medallion data pipeline (Bronze/Silver/Gold) featuring custom input file generation, automated multi-stage processing, and load-ready file export.
"# medallion-data-pipeline" 
## Step 1: Pre-loading & Data Generation

Before triggering the Databricks ingestion pipeline, synthetic raw data must be generated.

* **Type:** Pre-loading process (Data Seeding)
* **Script:** `seeds/generate_users_dirty_data_file.ipynb`
* **Description:** Simulates raw source data by generating synthetic user records containing deliberate quality issues (missing fields, inconsistent formats).
* **Destination:** Writes files to `user_dirty_files` for S3 upload (`s3://dirtyusersplacement/main_file`), ready for the Bronze layer.
