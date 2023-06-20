# EKS-S3_bucket

Step1: >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

create a S3 bucket and upload a file


Step 2: >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

create the identity provider if not available

copy the OpenID connect provider from the EKS overview page and go to IAM >>> Identity Provider >>> OpenID connect

paste the provicer url which copied in above step.
audience: sts.amazonaws.com

Step 3>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

create a role and select web-identity and select identity provider 
and provide the read or write S3 policy

Step 4: >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

Create the service account and mention the above role url 

Step 5: >>>>>>>>>>>>>>>>>>>>>>>>>>>>

create the pod and use the above service account and check the logs if it is working.

kubectl logs pod-name -c init-container-name

