# CFTemplate

A cloudformation template that accepts user inputs as parameters where applicable ( for example, Admin password). This template should setup VPC, create subnets, launch a CM instance, pull the necessary code (modules, classes, recipes etc) from a GIT repo (or S3), and configure the web instance for basic Drupal or Wordpress setup.

# Steps to run template 
1. Install aws cli on machine.
2. Clone the repository
	git clone https://github.com/Ramesh7/CFTemplate.git
3. Goto CFTemplate and run following command : 

aws cloudformation create-stack  --stack-name ReanCloudAssignment  \
    --template-body template/CFTemplate.json \
    --parameters  ParameterKey=AmiID,ParameterValue=<ami-id> ParameterKey=InstanceType,ParameterValue=t1.micro ParameterKey=KeyName,ParameterValue=<aws-key> ParameterKey=Region,ParameterValue=us-east-1
	
	