# digital-twin-aws
A conversational AI that represents you (or anyone you choose) and can interact with visitors on your behalf

This repo is based on the guideline by `Ed Donner's` [production repo](https://github.com/ed-donner/production/tree/main/week2) which is used at his [Udemy AI Engineering Production Track](https://www.udemy.com/course/generative-and-agentic-ai-in-production) course.


# Getting Started

## Create .env file
```
# AWS Configuration
AWS_ACCOUNT_ID=your_Aws_account_id
DEFAULT_AWS_REGION=your_region

# Project Configuration
PROJECT_NAME=twin
```

## Initialize terraform
```
cd terraform
terraform init
```
That will initialize terraform in your local dir.

## Now deploy dev environment

```
$ ./scripts/deploy.sh dev
```

It will deploy everything at AWS using `terraform apply`, after the deployment it will show you the cloudfront url click on it and that's it, Your digital twin will be shown. 

## Destroy Environment
Once you are done with testing, you can destroy it:
```
# Destroy dev environment
$ ./scripts/destroy.sh dev
```

This will run `terraform destroy` to destroy the aws resources.