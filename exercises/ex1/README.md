# Exercise 1 - Configure SAP Edge Services

In Exercise 1, we will create a SAP Edge Services project.  A project is an aggregation of entities such as sensor models, rules, rule data sources, actions, connectors, and runtime settings where you can define and manage each entity and publish the project to create a configuration for the Streaming Service.      After you complete Exercise 1, you will then move to Exercise 2 to deploy such streaming service configuation on the gateway to automatically trigger the cretion of a work order based on live IoT sensor data.

## Exercise 1.1 Create an Edge Designer Project

After completing these steps you will have created an edge designer project.

1. Log onto SAP Edge Services.
<br>![](/exercises/ex1/images/Ex1_Step1_1.png)

   Note: After logon you will land on the main SAP Edge services screen.

2. Click the Edge Designer tile.
<br>![](/exercises/ex1/images/Ex1_Step1_2.png)

3. Click + to add a new project.
<br>![](/exercises/ex1/images/Ex1_Step1_3.png)

   Note: A project is an aggregation of entities such as sensor models, rules, rule data sources, actions, connectors, and runtime settings where you can define and manage each entity and publish the project, which creates a configuration for the Streaming Service.

4. Enter the following details in the next screen, and click Create.
<br>Please Note: Throughout the tutorial you must replace XX with your own assigned number<br>
- Name: __TrainingXX__
- Description: __TrainingXX__
- Profile Delimiter:	__>>>__


## Exercise 1.2 Sub Exercise 2 Description

After completing these steps you will have...

1.	Enter this code.
```abap
DATA(lt_params) = request->get_form_fields(  ).
READ TABLE lt_params REFERENCE INTO DATA(lr_params) WITH KEY name = 'cmd'.
  IF sy-subrc <> 0.
    response->set_status( i_code = 400
                     i_reason = 'Bad request').
    RETURN.
  ENDIF.

```

2.	Click here.
<br>![](/exercises/ex1/images/01_02_0010.png)

```abap
response->set_text( |Hello World! | ). 
```
## Summary

You've now ...

Continue to - [Exercise 2 - Exercise 2 Description](../ex2/README.md)

