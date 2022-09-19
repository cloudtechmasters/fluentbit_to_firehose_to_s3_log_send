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

helm repo add eks https://aws.github.io/eks-charts

    # helm repo add eks https://aws.github.io/eks-charts
    "eks" has been added to your repositories

helm upgrade --install aws-for-fluent-bit --namespace kube-system eks/aws-for-fluent-bit --values values.yaml

    # helm upgrade --install aws-for-fluent-bit --namespace kube-system eks/aws-for-fluent-bit --values values.yaml
    WARNING: Kubernetes configuration file is group-readable. This is insecure. Location: /root/.kube/config
    WARNING: Kubernetes configuration file is world-readable. This is insecure. Location: /root/.kube/config
    Release "aws-for-fluent-bit" does not exist. Installing it now.
    W0919 15:06:57.508222    3592 warnings.go:70] policy/v1beta1 PodSecurityPolicy is deprecated in v1.21+, unavailable in v1.25+
    W0919 15:06:57.612890    3592 warnings.go:70] policy/v1beta1 PodSecurityPolicy is deprecated in v1.21+, unavailable in v1.25+
    NAME: aws-for-fluent-bit
    LAST DEPLOYED: Mon Sep 19 15:06:56 2022
    NAMESPACE: kube-system
    STATUS: deployed
    REVISION: 1
    TEST SUITE: None
    NOTES:
    aws-for-fluent-bit has been installed or updated. To check the status of pods, run:

    kubectl get pods -n kube-system
