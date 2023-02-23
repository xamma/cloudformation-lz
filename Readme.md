# AWS Cloudformation Landingzone
Small IaC example for a simple Landingzone on AWS, including an EC2-instance, Networking, SSH-Key an SGs.  
This is especially meant for comparing the differences to launching ressources with Terraform and the AWS Provider.  

## Setup
Clone project and cd into it.  

### Configure AWS CLI
```
aws configure
```
Paste in your **ACCESS_KEY** and **SECRET_ACCESS_KEY**.  

### Create resources
```
aws cloudformation create-stack --stack-name test-stack-01 --template-body file://cloudformation-lz-stack.yaml
```

### Delete resources
```
aws cloudformation delete-stack --stack-name test-stack-01
```