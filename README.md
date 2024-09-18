# Azure-end-to-end-pipeline-project

Lets suppose a third party service drops a file "orders.csv" in datalake storage. The name of the folder is "landing" in ADLS gen 2.


I need to perform two checks:
1. Make sure the column "order_id" is unique.
2. The order_status can only have a definite range of values
