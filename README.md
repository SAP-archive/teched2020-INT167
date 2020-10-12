# INT167 - Implement and Run Business Scenarios at the Edge Using SAP Edge Service

## Description

This repository contains the material for the SAP TechEd 2020 session 1243 - Implement and Run Business Scenarios at the Edge Using SAP Edge Services.  

## Overview

This session introduces attendees to SAP Edge Services, which brings together local compute, persitency and business transactions at the edge.  SAP Edge Services enables powerful microservices to be deployed at the edge but orchestrated from the cloud to extend the processing power of the cloud to an edge location.   An edge location could be a remote oil rig, a mining site, a moving vessel or a manufacturing plant, where edge services are deployed at edge gateways to allow local compute, local persisteny and local business transaction execution.

Throughout the following exercises, you will be working with the following components of SAP Edge Services:
- Policy Service, which provides orchestration & lifecycle management of edge services from the cloud
- Streaming Service, which analyzes IoT data streams in real-time based on business logic
- Essential Business Functions Service, which provides business context (data and processes) at the edge despite challenges of connectivity, latency or bandwidth.

## Requirements

The requirements to follow the exercises in this repository are:
- You need to have a laptop or PC with a browser

## Exercises

The following two exercises are designed to help you gain hands-on experience in building and executing a real-world scenario: Leverage SAP Edge Services to automatically create a Work Order based on device IoT sensor data at a plant.

- [Exercise 1 - Configure SAP Edge Services](exercises/ex1/)
    - [Step 1.1 - Create an Edge Designer Project](exercises/ex1#step-11-create-an-edge-designer-project)
    - [Step 1.2 - Add data model to project](exercises/ex1#step-12-Add-data-model-to-project)
    - [Step 1.3 - Define action](exercises/ex1#step-13-Define-action)
    - [Step 1.4 - Define rule](exercises/ex1#step-14-Define-rule)
    - [Step 1.5 - Define runtime settings](exercises/ex1#step-15-Define-runtime-settings)
    - [Step 1.6 - Define connector settings](exercises/ex1#step-16-Define-connector-settings)
    - [Step 1.7 - Publish project](exercises/ex1#step-17-Publish-project)
- [Exercise 2 - Deploy and Test SAP Edge Services to Automatically Create a Work Order based on IoT Sensor Data](exercises/ex2/)
    - [Step 2.1 - Deploy project to gateway](exercises/ex2#step-21-Deploy-project-to-gateway)
    - [Step 2.2 - Verify deployment in SAP Edge Gateway](exercises/ex2#step-22-Verify-deployment-in-SAP-Edge-Gateway)
    - [Step 2.3 - Simulate device](exercises/ex2#step-23-Verify-Simulate-device)
    - [Step 2.4 - Trigger rule and create work order](exercises/ex2#step-24-Trigger-rule-and-create-work-order)
    
    
**IMPORTANT**

Your repo must contain the .reuse and LICENSES folder and the License section below. DO NOT REMOVE the section or folders/files. Also, remove all unused template assets(images, folders, etc) from the exercises folder. 

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2020 SAP SE or an SAP affiliate company. All rights reserved. This file is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
