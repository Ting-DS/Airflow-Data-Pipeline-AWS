# Airflow-Data-Pipeline & AWS

<div align="center">
  <img src="https://github.com/Ting-DS/Airflow-Data-Pipeline/blob/main/image/AirflowAWS.jpeg" width="60%">
</div>

## Introduction
Sparkify is a music streaming company, aims to enhance automation and monitoring in their **data warehouse ETL** (Extract, Transform, Load) pipelines. They've chosen [Apache Airflow](https://airflow.apache.org/) as the tool for this purpose. I create advanced data pipelines with dynamic, reusable tasks, monitoring capabilities, and support for easy backfills. Additionally, ensuring **data quality** is crucial, so plan to run tests on their datasets post-ETL to detect any discrepancies. The source data is stored in [AWS S3](https://aws.amazon.com/pm/serv-s3/?trk=fecf68c9-3874-4ae2-a7ed-72b6d19c8034&sc_channel=ps&ef_id=EAIaIQobChMIiqPSj8TJgQMV-yezAB0VAwcmEAAYAiAAEgL8MPD_BwE:G:s&s_kwcid=AL!4422!3!536452728638!e!!g!!aws%20s3!11204620052!112938567994) and must be processed in Sparkify's [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/) data warehouse. The source datasets include JSON logs detailing user activity and JSON metadata about the songs users listen to. As a data engineer, I will create custom operators to perform tasks such as staging the data, filling the data warehouse, and running checks on the data quality as the final step.

## Project Airflow DAG 

[picture]

## Instuction
 - Create IAM user in AWS and Configure Redshift Serverless and S3 bucket (Note: same region).
 - Connect Airflow to AWS Redshift by Airflow Web-UI.
 - Make sure the path is correct in your airflow workspace, run the following commands in the 
terminals to access the Airflow UI:
   ```
   /opt/airflow/start-services.sh
   /opt/airflow/start.sh
   airflow users create --email student@example.com --firstname aStudent --lastname aStudent --        password admin --role Admin --username admin
   airflow scheduler
   ```

