# Work in Progress: README.md

Note: This README is a work in progress and serves more as a reference guide. All private information has been removed.

## Overview

This repository contains a set of files that are used for setting up and managing a Kinesis Video Stream (KVS) integrated with AWS IoT for a camera stream named "kvs_camera_stream". The files provide the necessary certificates, keys, and policies for secure communication and authorization within AWS services.

### File Descriptions

- `cacert.pem`: This is the Certificate Authority (CA) certificate used to ensure secure communication between the client and the server.
- `certificate`, `certificate.pem`: These are likely the public certificate files for the IoT device or service that's interacting with AWS IoT.
- `cli_deploy_scripts.txt`: Contains CLI deployment scripts that automate some aspects of the infrastructure setup or deployment.
- `iam-permission-document.json`, `iam-policy-document.json`, `iam-role.json`: These JSON files define the permissions, policies, and roles for the AWS Identity and Access Management (IAM) service, which governs what actions services and users can perform.
- `iot-credential-provider.txt`, `iot-policy-document.json`, `iot-role-alias.json`, `iot-thing.json`, `iot-thing-type.json`: These files are related to the setup and configuration of AWS IoT entities such as policies, roles, and IoT devices (things).
- `private.pem.key`, `public.pem.key`: These are the private and public keys used for encryption and decryption of communication.
- `token.json`: This file is likely used to store the temporary credentials received from the AWS IoT credentials provider.

### CLI Commands

- `iot attach-thing-principal`: Attaches a principal (such as a certificate) to an IoT thing (device), in this case, a camera stream.
- `kinesisvideo create-stream`: Creates a Kinesis Video Stream with a specified data retention policy and stream name.

### Security Policy Example

The provided security policy example indicates a policy that allows the AWS Budgets service to publish messages to an SNS topic. This suggests part of the system may involve monitoring and managing AWS service budgets.

## Summary

The combination of these files and CLI commands serves the purpose of this repository is to:

1. Setup a secure camera streaming service using AWS IoT and Kinesis Video Stream.
2. Attach necessary certificates and keys to the AWS IoT thing (the camera stream).
3. Secure the communication and define the permissions for the AWS services interacting with the IoT device.
4. Manage and monitor the cost associated with the services via AWS Budgets.
