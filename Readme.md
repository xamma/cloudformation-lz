# AWS Cloudformation Landingzone
Small IaC example for a simple Landingzone on AWS, including an EC2-instance, Networking, SSH-Key an SGs.  
This is especially meant for comparing the differences to launching ressources with Terraform and the AWS Provider.  
Especially the ***state-management*** and ***drift-detection*** is a big difference.  

This stack is written with Parameters, so you can add your custom configuration with the 
```--parameters ParameterKey1=ParameterValue1 ParameterKey2=ParameterValue2 ...``` option.  

The stack will take the in the AWS CLI configured region as default.  

## Setup
Clone project and cd into it.  

### Configure AWS CLI
```
aws configure
```
Paste in your **ACCESS_KEY** and **SECRET_ACCESS_KEY**.  

### Validate stack
```
aws cloudformation validate-template --template-body file://cloudformation-lz-stack.yaml
```

### Create resources
```
aws cloudformation create-stack --stack-name test-stack-01 --template-body file://cloudformation-lz-stack.yaml
```

### Get stack information (outputs etc.)
```
aws cloudformation describe-stacks --stack-name test-stack-01
```

### Delete resources
```
aws cloudformation delete-stack --stack-name test-stack-01
```