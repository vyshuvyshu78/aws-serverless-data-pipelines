import json
import boto3
import logging
import os

logger = logging.getLogger()
logger.setLevel(logging.INFO)

glue_client = boto3.client('glue')

def lambda_handler(event, context):
    try:
        job_name = os.environ.get("GLUE_JOB_NAME", "jobname")
        
        response = glue_client.start_job_run(JobName=job_name)
        
        logger.info(f"Started Glue Job: {job_name}")
        logger.info(f"Run ID: {response['JobRunId']}")
        
        return {
            "statusCode": 200,
            "body": json.dumps("Glue job started successfully")
        }

    except Exception as e:
        logger.error(f"Error starting Glue job: {str(e)}")
        raise e
