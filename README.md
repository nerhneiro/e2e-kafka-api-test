## Kafka compatibility test

This test is written for the [YDB project](https://github.com/ydb-platform/ydb). It allows to check the work of YDB Topics with Kafka API using Kafka Streams and checks the correct work of transactions.

* The test builds a kafka stream that consumes data from the source topic and produces it to the target topic.
* At the same time a *ydb workload topic run write* is launched, so some data is continuously being written to the source topic.
* After the data is fully produced to the source topic, after some wait the check starts. It compaires total message count in source and target topics and verifies if they are equal (as it should be).

To repeat this test on your own you can run the following python script: *the link will be here*. You need to create a virtual environment and install all the required libraries, including YDB python sdk and YDB CLI.
