+++
title = "Request to AWS service"
weight = 1
chapter = false
pre = "<b>1.1 </b>"
+++

#### Request to AWS service

- **Request**: When a principal tries to perform an operation using the AWS Console, AWS API, or AWS CLI, that principal must send a request. Request information includes
  - **Action** or **Operation**: the action the principal wants to perform.
  - **Resource**: resource information will be affected
  - **Principal**: information about the person or application sending the request, including policy information attached to that principal
  - **Environment data**: information about IP address, user agent, SSL enable status and time to send request
  - **Resource data**: information related to the resource that can be requested. For example the name of the DynamoDB data table, or the tag name of the EC2 virtual machine