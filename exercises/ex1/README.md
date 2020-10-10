# Exercise 1 - Configure SAP Edge Services

In Exercise 1, we will create a SAP Edge Services project.  A project is an aggregation of entities such as sensor models, rules, rule data sources, actions, connectors, and runtime settings where you can define and manage each entity and publish the project to create a configuration for the Streaming Service.      After you complete Exercise 1, you will then move to Exercise 2 to deploy such streaming service configuation on the gateway to automatically trigger the cretion of a work order based on live IoT sensor data.

## Step 1.1 Create an Edge Designer Project

After completing these steps you will have created an edge designer project.

1. Log onto SAP Edge Services.
<br>![](/exercises/ex1/images/Ex1_Step1_1.png)

   Note: After logon you will land on the main SAP Edge services screen.

2. Click the Edge Designer tile.
<br>![](/exercises/ex1/images/Ex1_Step1_2.png)

3. Click __+__ to add a new project.
<br>![](/exercises/ex1/images/Ex1_Step1_3.png)

   Note: A project is an aggregation of entities such as sensor models, rules, rule data sources, actions, connectors, and runtime settings where you can define and manage each entity and publish the project, which creates a configuration for the Streaming Service.

4. Enter the following details in the next screen, and click Create.
<br>Note: Throughout the tutorial you must replace __XX__ with __your own assigned number__<br>
   - Name: __TrainingXX__
   - Description: __TrainingXX__
   - Profile Delimiter: __>>>__
<br>![](/exercises/ex1/images/Ex1_Step1_4.png)

## Step 1.2 Add data model to project

After completing these steps you will have added data model to the project you just created.

1.	Click __Data Model__, and then press __+__.
<br>![](/exercises/ex1/images/Ex1_Step2_1.png)
In SAP IoT, we have already defined a sensor type __Boiler__, which you are going to use in this project. The Boiler sensor type has two capabilities: __Temperature__ and __Pressure__

2.	Select the following values from the dropdown, and then click __Create__:
   - Sensor Type: __Boiler__
   - Capability Name: __BoilerTraining__
   - Temperature: __Check Box Checked__
<br>![](/exercises/ex1/images/Ex1_Step2_2.png)

3. Fidelity enables you to configure the SAP Edge Services to selectively send IoT data to cloud (or other target applications) or save at the edge in the configured time interval.

   To set fidelity, select your data model and click __Fidelity__.
<br>![](/exercises/ex1/images/Ex1_Step2_3_1.png)

   Set the __Edge Fidelity__ and the __Outbound Fidelity__ to __Enabled__, and enable __IoT Service Cloud Connector__.

   <br>Click __Save__.
<br>![](/exercises/ex1/images/Ex1_Step2_3_2.png)   

4. Click __Validate__ at the top-right.
   <br>After a successful validation your screen should look like this:
<br>![](/exercises/ex1/images/Ex1_Step2_4.png)   

## Step 1.3 Define action

After completing these steps you will have defined an action that will trigger the creation of the work order. The action will be triggered by a streaming rule that will be created later.

1. Select __Actions__, and then click __+__ to the right.
<br>![](/exercises/ex1/images/Ex1_Step3_1.png)   

2. Enter the following values for your action, and then click __Save__.
   - Action Name: __Create Work Order__
   - Description: __Create Work Order__
   - Action Type: Select from Drop Down __Create Work Order__
   - Device ID: __${deviceId}__
   - Subject: __${deviceId} : Temperature too high__
   - Remarks: __${deviceId} : Temperature too high__
   - Main Work Center: __RES-0100__
<br>![](/exercises/ex1/images/Ex1_Step3_2.png) 

## Step 1.4 Define rule

After completing these steps you will have defined a rule that will trigger the action we created in the previous step.

1, Click Rules, and then click +.

## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

