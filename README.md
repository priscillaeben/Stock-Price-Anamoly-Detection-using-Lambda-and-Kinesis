Stock Price Anamoly Detection using Lambda and Kinesis
********** Cloud AWS Project *****************

**lambdafunction.py**

In this I have used boto3 for connecting SNS to my topic StockVariation. This topic is subscribed with my email id. This lambda function captures the data from Kinesis data stream and process it to extract the data. Here we have extracted the stock close price, 52 week high and 52 week low prices. Based on the variance 80% and 120%, this will push a message to SNS. So that same will be delivered to the subscribed email id.

**StockPriceIngestion.py**

In this we have used Yahoo finance API to pull the data and process it to extract stock id, price, timestamp, 52 week high and 52 week low. Then we are constructing it as a json and sending it to Kinesis Data Stream using boto3.

**Learnings from this project**

I have understood the working area of following AWS functions through this project

* AWS EC2
* AWS CLI
* AWS Kinesis
* AWS SNS
* AWS Lambda
