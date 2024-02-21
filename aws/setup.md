# AWS Setup Guide for Smart Automated Irrigation System

This document outlines the steps required to configure AWS IoT Core, AWS Lambda, and other necessary AWS services for the Smart Automated Irrigation System.

## Prerequisites

- An AWS account.
- AWS CLI installed and configured on your computer.
- Basic knowledge of AWS services.

## 1. AWS IoT Core Setup

### Create a Thing

1. **Log in** to the AWS Management Console.
2. Navigate to **AWS IoT Core** dashboard.
3. In the **Manage** section, click on **Things** and then **Create**.
4. Follow the wizard to create a new thing for your device (e.g., `IrrigationController`).

### Register a Certificate

1. In the **Secure** section, select **Certificates** and click **Create**.
2. Follow the prompts to create a new certificate. Download the certificate, private key, and root CA.
3. Attach the certificate to your Thing.

### Create and Attach a Policy

1. In the **Secure** section, select **Policies** and click **Create**.
2. Create a policy that allows your device to connect, publish, subscribe, and receive.
3. Attach the policy to your certificate.

## 2. Setting Up a LoRaWAN Gateway

If you're using a LoRaWAN gateway, follow the manufacturer's instructions to set it up and ensure it's connected to AWS IoT Core.

## 3. AWS Lambda Functions

### Create a Lambda Function

1. Navigate to the **AWS Lambda** console.
2. Click **Create function** and choose **Author from scratch**.
3. Enter a name for your function (e.g., `IrrigationDecisionFunction`).
4. Choose an execution role that has permissions to access AWS IoT and any other required services.
5. Use the provided code snippets in the `lambda_functions` directory of this project to define your function's logic.

### Set Up Triggers

1. Configure your Lambda function to trigger on IoT Core events, such as receiving a message from your device.
2. Use the **Add trigger** option in the Lambda function configuration, selecting AWS IoT as the source.

## 4. Additional Services

### DynamoDB

If storing sensor data for historical analysis:

1. Navigate to the **DynamoDB** console.
2. Click **Create table** and define your table's primary key (e.g., `SensorID` and `Timestamp`).

### API Gateway

For remote access to your Lambda functions or to expose an API:

1. Go to the **API Gateway** console.
2. Create a new API and define resources and methods based on your project's needs.

## 5. Testing

Ensure all components are properly configured by:
- Publishing a test message from your device.
- Verifying that the message triggers your Lambda function.
- Checking that the desired action (e.g., data storage, notification) occurs as expected.

## Troubleshooting

- Verify that all policies and roles have the correct permissions.
- Check the AWS CloudWatch logs for errors or messages from your Lambda functions.

