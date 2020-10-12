# Exercise 2 - Deploy and Test SAP Edge Services to Automatically Create a Work Order based on IoT Sensor Data

In this exercise, we will deploy and test an SAP Edge Services project, with streaming rules based on Iot data, that will automate creating a work order in S/4HANA.

## Step 2.1 Deploy project to gateway

After completing these steps you will have deployed the project you've just created to your Edge Gateway

1. Log onto SAP Edge Services.

   After logon, you will land on the main SAP Edge Services screen.
   
   Click on __SAP Edge Services Management__.

<br>![](/exercises/ex1/images/Ex2_Step1_1.png)

2. Select the gateway where you want to deploy your project (Gateway XX).

<br>![](/exercises/ex1/images/Ex2_Step1_2.png)

3. Select __Configurations__ and click __+__ on the right.

<br>![](/exercises/ex1/images/Ex2_Step1_3.png)

4. From the dropdown, select __Streaming Service__, for __Configuration__ select your published project, and then click __Apply__.

   If you followed the naming given in the first part of the tutorial, it should be named something like __TrainingXX-v__.

<br>![](/exercises/ex1/images/Ex2_Step1_4_1.png)

   The configuration will be downloaded to the gateway. This might take a few seconds.

   Click the refresh button on the right until you see the configuration status __Applied__.
   
<br>![](/exercises/ex1/images/Ex2_Step1_4_2.png)   

## Step 2.2 Verify deployment in SAP Edge Gateway

After completing these steps you will have verified that the deployment was done correctly.

1.	Go to __General Settings__ of your gateway, and click the __Edge Console URL__.

    __Important Note for Mac Users__ : Use the Safari browser for this part of the exercise. If you want to use any other browser make sure you import the server certificate into your Keychain Access app and modify the certificate trust to __Always Trust__

<br>![](/exercises/ex1/images/Ex2_Step2_1.png)   

    A new window will open and you will land on the logon page of the SAP Edge Services gateway.
    
2. Log on with the following credentials:

   - Name: __admin__
   - Password: __AdminAdmin1__
   
<br>![](/exercises/ex1/images/Ex2_Step2_2.png)     

3. You should see a Sensor Profile named __BoilerTraining>>>2...3>>>Boiler ...__

   Please verify that both rules are enabled.

<br>![](/exercises/ex1/images/Ex2_Step2_3_1.png)   

   Under __Actions__, you should see your action __Create Work Order__.

<br>![](/exercises/ex1/images/Ex2_Step2_3_2.png)   

   Finally, verify under __Runtime Settings__ that you have unchecked the __Validate HTTPS Certificates__ flag.

<br>![](/exercises/ex1/images/Ex2_Step2_3_3.png)  

## Step 2.3 Simulate device

After completing these steps you will have tested end-to-end rule logic using the built-in emulated device and emulated sensor controls. The Live Sensors Emulation view displays all sensor profiles configured to Stream Readings to Monitor.

We will use this functionality to trigger the rule that we created in the previous tutorial. This rule will trigger the creation of the work order.

1. 


## Summary

You've now ...

