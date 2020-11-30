# Exercise 2 - Deploy and Test SAP Edge Services to Automatically Create a Work Order based on IoT Sensor Data

In this exercise, we will deploy and test an SAP Edge Services project, with streaming rules based on Iot data, that will automate creating a work order in S/4HANA.

## Step 2.1 Deploy project to gateway

After completing these steps you will have deployed the project you've just created to your Edge Gateway

1. Go to the Fiori Launch Pad for SAP Edge Services, and then click tile __SAP Edge Services Management__

```
   If you haven't logged onto SAP Edge Services, then follow step 1.1/1 in exercise #1 to log on first
```   
   
<br>![](/exercises/ex2/images/Ex2_Step1_1.png)

2. Select the gateway where you want to deploy your project (__Gateway XX, where XX is your assigned two-digit ID__ ).

<br>![](/exercises/ex2/images/Ex2_Step1_2.png)

3. Select __Configurations__ and click __+__ on the right.

<br>![](/exercises/ex2/images/Ex2_Step1_3.png)

4. From the dropdown, select __Streaming Service__, for __Configuration__ select your published project, and then click __Apply__.

   If you followed the naming given in the first part of the tutorial, it can be named something like __TechEdXX-V1__, __where XX is your assigned two digit ID__.  (e.g. TechEd08-V1, TechEd45-V2, etc.)

<br>![](/exercises/ex2/images/Ex2_Step1_4_1.png)

   The configuration will be downloaded to the gateway. This might take a few minutes, just wait until the "Add Configuration" pop up is dismissed.

   Keep clicking the __refresh button__ on the right until you see the configuration status has been changed to __Applied__, this might take another minute or two.
   
<br>![](/exercises/ex2/images/Ex2_Step1_4_2.png)   

## Step 2.2 Verify deployment in SAP Edge Gateway

After completing these steps you will have verified that the deployment was done correctly.

1.	Go to __General Settings__ of your gateway, and click the __Edge Console URL__.

```
   Important Note for Mac Users: Use the Safari browser for this part of the exercise. 
   If you want to use any other browser make sure you import the server certificate into your Keychain Access app
   and modify the certificate trust to Always Trust
```
<br>![](/exercises/ex2/images/Ex2_Step2_1.png)
    
   A new window will open and you will land on the logon page of the SAP Edge Services gateway.
      
2. Log on with the following credentials:

   - Name: __admin__
   - Password: __AdminAdmin1__
   
<br>![](/exercises/ex2/images/Ex2_Step2_2.png)     

3. You should see a Sensor Profile named __BoilerTraining>>>3>>>BoilerTraining>>>Temperature__

   Please verify that both rules are enabled.

<br>![](/exercises/ex2/images/Ex2_Step2_3_1.png)   

   Under __Actions__, you should see your action __Create Work Order__.

<br>![](/exercises/ex2/images/Ex2_Step2_3_2.png)   

   Finally, verify under __Runtime Settings__ that you have unchecked the __Validate HTTPS Certificates__ flag.

<br>![](/exercises/ex2/images/Ex2_Step2_3_3.png)  

## Step 2.3 Simulate device

After completing these steps you will have tested end-to-end rule logic using the built-in emulated device and emulated sensor controls. The Live Sensors Emulation view displays all sensor profiles configured to Stream Readings to Monitor.

We will use this functionality to trigger the rule that we created in the previous tutorial. This rule will trigger the creation of the work order.

1. Select the __Sensor Profiles__ option on the left and then your sensor profile.

2. Check the option __Stream Reading to Monitor__, and click __Save__.

<br>![](/exercises/ex2/images/Ex2_Step3_2.png)  

3. Now simulate sensor readings by doing the following:

   - Select __Live Sensors__ on the left sidebar.
   - Enter __Device_XX__ as the device under __Device ID__ , __where XX is your assigned two-digit ID.  e.g. Device_02, Device_18, etc.__.
   - Click the play button.
   
   You can move the slider to increase and decrease the value of the reading but keep it under 80 for now. The simulated values will start populating the screen.

   Remember that we defined a rule that will trigger when the temperature exceeds 80.

<br>![](/exercises/ex2/images/Ex2_Step3_3.png)  

## Step 2.4 Trigger rule and create work order

After completing these steps you will have triggered the rules and created a Work Order 

1. Move the slider to the right until it reaches a value over 80. Wait until you have 2 readings and slide the value back to under 80.

   You can now pause the emulator by pressing the Pause button.

<br>![](/exercises/ex2/images/Ex2_Step4_1.png) 

2. Now check if the temperature increase has triggered an event.

   Select __Events__ on the left sidebar. You should see an event called __Check Temperature__ (The event __Check Temperature__ will trigger the action __Create Work Order__).
   
<br>![](/exercises/ex2/images/Ex2_Step4_2_1.png)   
   
3. Verify the Work Order has been created.

   Log onto sample edge application for Essential Business Functions: https://ec2-100-24-131-108.compute-1.amazonaws.com:9443/dep/fiori2#Shell-home
   
   - User: __EBEF__
   - Password: __Initial__

<br>![](/exercises/ex2/images/Ex2_Step4_3_1.png) 

   Click the tile __Work Orders__ (under the tab "Plant Maitenance")

<br>![](/exercises/ex2/images/Ex2_Step4_3_2.png)   
   
   Click the newly generated work order at the top of the list 

<br>![](/exercises/ex2/images/Ex2_Step4_3_3.png) 

   You work order should look like this

<br>![](/exercises/ex2/images/Ex2_Step4_3_4.png) 
   

## Summary

You've now completed exercices of using SAP Edge Services to automatically create Work Order based on IoT data at the edge 

