# DEG Group 4 Capstone Project 


## Team members 

| Name | Email |
| ----------- | ----------- |
| Yamna Tahir | yamna.tahir@xloopdigital.com |
| Abdul Wassay Ansari | wassay.ansari@xloopdigital.com |
| Syed Hamza | syed.hamza@xloopdigital.com |
| Durraiyah Muneer | durraiyah.munir@xloopdigital.com |
| Usman Zaman | usman.zaman@xloopdigital.com |
| Rumaisa Shahab | rumaisa.shahab@xloopdigital.com |
| Hamza Hanif Alam | hamza.hanif@xloopdigital.com |



In the ETL pipeline, we managed streaming data from various sensors to predict occupancy status. The ingestion layer incorporated Kafka REST Proxy, FastAPI endpoints, and a Boto3 client to retrieve data from a Minio instance. Kafka served for asynchronous communication and fault tolerance, storing ingested data in the Kafka cluster.

The transformation layer employed PySpark and Kafka Python integrated seamlessly. Kafka Python, acting as consumers in a multithreaded environment, retrieved data from the Kafka cluster, and Spark transformed it. The transformed data was then input to an AI model trained for predicting occupancy status.

Post-predictions, the data seamlessly loaded into MongoDB hosted on the cloud using PyMongo. Concurrently, streaming data was presented on the front-end through a Flask app. The entire process adhered to a microservices architecture, utilizing Docker containerization for efficient deployment and scalabilit

