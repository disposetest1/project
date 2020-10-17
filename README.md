autoauto- [Operationalizing Machine Learnig](#operationalizing-machine-learnig)auto    - [Architectural Diagram](#architectural-diagram)auto    - [Key Steps](#key-steps)auto    - [Future Improvement.](#future-improvement)auto    - [Screen Recording](#screen-recording)autoauto



# Operationalizing Machine Learnig

In this project we are going to create and run an AUto ML Experiment. Its Best model will then be deployed and the Swagger documentation of the model will be accessed in order to consume and update write data through the model endpoints. A pipeline will the be created and published using the Python SDK.

## Architectural Diagram

![alt text](https://github.com/disposetest1/project/blob/master/architectural_diagram.jpg)



## Key Steps
**Create and Run AUtoML experiment** 

- Here we create a new Auto ML experiment with the Bank marketing data set.

![alt text](https://github.com/disposetest1/project/blob/master/1_registered_datasets.jpg)

  - We then run it to have the result as bellow.  

![alt text](https://github.com/disposetest1/project/blob/master/2_experiment_completed.jpg)



**Deploy the Best Model**

![alt text](https://github.com/disposetest1/project/blob/master/3_best_model.jpg)

- Once the experiment is created, you can select the best model which is first in the list of models under the models tab and the deploy it with authentication enabled.


**Enable Application Insights**

- Here azure python SDK is used to run the "logs.py" script found in the project root directory. 

![alt text](https://github.com/disposetest1/project/blob/master/5_enabled_logging.jpg)

- Application insights and logging are now enabled the deployed model.

![alt text](https://github.com/disposetest1/project/blob/master/4_application_insigths_enabled.jpg)


**Swagger Documentation**

- Here , the swagger documentation of the model is accessed on the local machine by running python scripts.

![alt text](https://github.com/disposetest1/project/blob/master/6_swagger.jpg)


**Consume the model endpoints**

- Here Information from the swagger documentation is used in order to consume the deployed model by executing the "endpoit.py" file that sends a POST HTTP request cotaining JSON DATA payload.

![alt text](https://github.com/disposetest1/project/blob/master/7_endpoint_output.jpg)


**Create publish and run pipeline**

- Here a pipeline for the model is created and ran with result as seen bellow.

![alt text](https://github.com/disposetest1/project/blob/master/8_pipeline_created.jpg)


- The pipeline is also published, all this using the python SDK and  a JYUPITER playbook  which makes use of the bank marketing data set;

![alt text](https://github.com/disposetest1/project/blob/master/10_bankmarketing_dataset.jpg),

- Once the pipeline have been published, The pipeline endpoint is made available;

![alt text](https://github.com/disposetest1/project/blob/master/9_pipeline_endpoint.jpg),

- The published pipeline overview should be as seen bellow;

![alt text](https://github.com/disposetest1/project/blob/master/11_published_pipeline_overview.jpg),

- Move to pipeline to see further Scheduled/Completed runs;

![alt text](https://github.com/disposetest1/project/blob/master/13_scheduled_runs.jpg),



## Future Improvement. 
- Make use of Python SDK to train the models, build and run pipelines  in a "write once use always" infrastructure as code way.
- To improve this project in the futur, a deeper and more accurate experiment should be created in order to have better model results.

## Screen Recording
https://youtu.be/wbO601xOD90