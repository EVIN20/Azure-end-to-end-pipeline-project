# Azure-end-to-end-pipeline-project

Lets suppose a third party service drops a file "orders.csv" in datalake storage. The name of the folder is "landing" in ADLS gen 2.


I need to perform two checks:
1. Make sure the column "order_id" is unique.
2. The "order_status" can only have a definite range of values that is if the values in "order_status" contain any value other than 
|"ON_HOLD|
|PENDING_PAYMENT|
|     PROCESSING|
|         CLOSED|
| PAYMENT_REVIEW|
|SUSPECTED_FRAUD|
|       COMPLETE|
|        PENDING|
|      CANCELLED|
it should be moved from "landing" folder to "staging" folder


## Steps followed
Step1: Create an ADLS gen2 storage account with 3 directories:
1. Landing-> Where the data is initially present/arrives.
2. Staging-> If the data passes the validation checks it is moved to staging folder.
3. Discarded-> If the data fails the validation checks it is moved to discarded folder.

![image](https://github.com/user-attachments/assets/88883fcb-795a-4a6b-b87a-a7332a4f9a76)

Step2: Making a databricks workspace for the data to be transformed.

Step3: Making a Azure data factory account for data transfer.

Step4: Creating "key vault" resource for storing confidential files.

Step5: Making a linked service for storage,databricks and key vault.

![image](https://github.com/user-attachments/assets/0a508098-9280-451f-bd7b-9bd1d75fce0f)











