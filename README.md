This project deals with downloading the files from git using ADF(Azure data factory)

Resources needed in azure:

Resource group
Storage account
Azure data factory
Azure data bricks

Steps:

1) Create a storage account azuredeproject1603 with hierarchal namespace 
2) Create a container inside with tokyo-olympics-data. Create two folders - raw-data/transformed-data
3) Create ADF and launch the azure ADF studio
4) Create a pipeline - drag the copy data command. Create a link service for HTTP type by pasting the url of the coaches.csv/medal.csv in data folder.
5) Set the sink to azure data lake azuredeproject1603 in raw-data folder.
6) Continue the same step for medals.csv and connect both the pipelines.
7) Once pipeline is created, run the pipeline after validating and then hit debug to run it.
8) Monitor pipeline if its successful and look for the files in raw-folder
9) Create an app registration- use it to create a secret key. Copy secret key, tenant id, client id and keep it safe with you. Go to azure blob and search for IAM and give azure blob access to app registration.
10) You need to use the keys and ids in databricks.
11) Create a compute cluster with single node - standard_DS3_V2
12) Use ipynb to do transformation the data by attaching the cluster and also put back the transformed data
13) Check the transformed folder. 
14) Delete all the resources that's not needed from azure.