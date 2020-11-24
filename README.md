# INT167 - Implement and Run Business Scenarios at the Edge Using SAP Edge Service

## Description

This repository contains the material for the SAP TechEd 2020 session 1243 - Implement and Run Business Scenarios at the Edge Using SAP Edge Services.  

## Overview

This session introduces attendees to SAP Edge Services, which brings together local compute, persitency and business transactions at the edge.  Before getting into the exercises, let's start with a quick overview.

- Value Drivers for Edge Computing: 
  - Devices and sensors produce more data than what can be (economically) transmitted to the cloud
  - Devices and sensors are in locations with intermittent connectivity, or restricted/costly bandwidth 
  - Decisions based on sensor data have to be made in real-time, i.e. crane collision detection and reaction can not wait for round trip latency to the Cloud
<br>![](/exercises/ex0/images/Ex0_1.png)  
 
- SAP Edge Services - Solution Capabilities:
  - SAP Edge Services enables powerful microservices to be deployed at the edge but orchestrated from the cloud to extend the processing power of the cloud to an edge location.   
  - The following diagram illutrates the core services provided by SAP Edge Services, some of which you will be working with throughout the exercises
    - __Policy Service__, which provides orchestration & lifecycle management of edge services from the cloud
    - __Streaming Service__, which analyzes IoT data streams in real-time based on business logic
    - __Essential Business Functions Service__, which provides business context (data and processes) at the edge despite challenges of connectivity, latency or bandwidth.
    - __Persistence Service__, which provides local storage of IoT data on IoT gateways
    - __Custom Edge Services__, e.g. Predictive Analytics Service, which can be deployed and executed at the edge gateway
<br>![](/exercises/ex0/images/Ex0_2.png)

## Requirements

The requirements to follow the exercises in this repository are:
- You need to have a laptop or PC with a browser

## Exercises

The following two exercises are designed to help you gain hands-on experience in building and executing a real-world scenario: Leverage SAP Edge Services to automatically create a Work Order based on device IoT sensor data at a plant.

- [Exercise 0 - Get Your Participant ID and Edge Services Access Credential](exercises/ex0/)
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
    - [Step 2.3 - Simulate device](exercises/ex2#step-23-Simulate-device)
    - [Step 2.4 - Trigger rule and create work order](exercises/ex2#step-24-Trigger-rule-and-create-work-order)
    
    
## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2020 SAP SE or an SAP affiliate company. All rights reserved. This file is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
