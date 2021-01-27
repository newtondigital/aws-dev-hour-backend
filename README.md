# AWS Dev Hour - Series 1 Demo Application (Backend)
### Type: Demo
### Repository:  https://github.com/aws-samples/aws-dev-hour-backend

## AWS Dev Hour - On Twitch
Do you have the skills it takes to build modern applications that are distributed and designed for scale and agility? If you’re interested in learning to build cloud native applications and architecture practices, join us for AWS Dev Hour: Building Modern Apps, a weekly Twitch show presented by AWS Training and Certification. Built by developers for developers, the series offers a hands-on approach. Over the course of 8 episodes, AWS expert hosts Ben Newton and May Kyaw will take you through the end-to-end build of a serverless application in the AWS cloud. You’ll have the chance to learn by doing, following along with the hosts and developing a cloud-native application using the AWS free tier. You’ll learn best practices for modern applications and better understand how AWS cloud-native applications differ from on-premises. Throughout the series, you’ll receive code, white papers, links to documentation, and other resources to help you progress. 

### Please note: this repository is for the BACKEND If you are looking for the React Frontend, please go to: 
[React Front End](https://github.com/aws-samples/aws-dev-hour-frontend)

## Architecture
<img width="1042" alt="architecture-screenshot" src="https://awsdevhour.s3-accelerate.amazonaws.com/architecture.jpg">

## Episodes

During each episode, we will be progressively building this full-stack application together. Please see the following URL for schedule and episode details: 

[AWS Dev Hour Schedule](https://pages.awscloud.com/traincert-twitch-dev-hour?sc_icampaign=event_twitch_devhour_launch_hosts&sc_channel=sm)


### Services used during the series:

- Amazon Cognito
- Amazon S3
- Amazon Simple Queue Service
- AWS Lambda
- Amazon DynamoDB
- Amazon Rekognition
- AWS Cloud Development Kit
- Amazon API Gateway
- AWS CodeBuild
- AWS CodePipeline

## Useful commands

 * `npm install`     install packages
 * `cdk synth`       emits the synthesized CloudFormation template
 * `cdk deploy`      deploy this stack
 * `cdk diff`        compare deployed stack with current state

 The `cdk.json` file tells the CDK Toolkit how to execute your app.

## Prerequisites

All CDK developers need to install Node.js 10.3.0 or later, even those working in languages other than TypeScript or JavaScript. The AWS CDK Toolkit (cdk command-line tool) and the AWS Construct Library run on Node.js. The bindings for other supported languages use this back end and tool set. We suggest the latest LTS version.

```bash
aws configure
npm -g install typescript
npm install -g aws-cdk
```
If you have not yet done so, you will also need to bootstrap your account:

```bash
cdk bootstrap aws://ACCOUNT-NUMBER-1/REGION-1
```

for example:

```bash
cdk bootstrap aws://123456789012/us-east-1
```


For further information, please see:

https://docs.aws.amazon.com/cdk/latest/guide/getting_started.html

https://docs.aws.amazon.com/cdk/latest/guide/bootstrapping.html

## Getting Started

1. `npm install` 

2. Create your AWS Lambda Layer assets (See note below)

3. `cdk deploy`

A 'cdk deploy' will deploy everything that you need into your account

4. You may now test the backend by uploading an image into your Amazon S3 bucket. 

## Cleanup

To clean up the resources created by the CDK, run the following commands:
```bash
cdk destroy
```
(Enter “y” in response to: Are you sure you want to delete (y/n)?).

## Tweaks

Rekognition confidence is currently set in the rekognition lambda. 
```python
minConfidence = 50
```  
Feel free to adjust and experiment. 
If you change, make sure to perform another 'cdk deploy' to update the lambda function. 

### Contributions

We would encourage all of our AWS Dev Hour viewers to contribute to this project. For more details, please refer to 'CONTRIBUTING.md'.

### License

This software is licensed under the Apache License, Version 2.0.