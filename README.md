# fluentbit_to_firehose_to_s3_log_send
fluentbit_to_firehose_to_s3_log_send

Steps:
======
1. Create s3 bucket to send logs from kinessis delivery stream
2. Create kinessis delivery stream
3. Deploy eks-fluentbit on eks cluster
4. Verify logs coming to s3 or not
5. Deploy Elastic Search and Kibana
6. Send Log from s3 to Elastic Search
