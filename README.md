# Operationalizing Machine Learning

# Table Of Contents

- [Operationalizing Machine Learnig](#operationalizing-machine-learnig)    
- [Architectural Diagram](#architectural-diagram)    
- [Key Steps](#key-steps)    
- [Future Improvement.](#future-improvement)    
- [Screen Recording](#screen-recording)



# Overview

In this project, we are going to create and run an AUto ML Experiment. Its Best model will then be deployed and the Swagger documentation of the model will be accessed to consume and update write data through the model endpoints. A pipeline will be created and published using the Python SDK.

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

- Once the experiment is created, you can select the best model which is first in the list of models under the model's tab and then deploy it with authentication enabled.


**Enable Application Insights**

- Here azure python SDK is used to run the "logs.py" script found in the project root directory. 

![alt text](https://github.com/disposetest1/project/blob/master/5_enabled_logging.jpg)

- Application insights and logging are now enabled in the deployed model.

![alt text](https://github.com/disposetest1/project/blob/master/4_application_insigths_enabled.jpg)


**Swagger Documentation**

- Here, the swagger documentation of the model is accessed on the local machine by running python scripts.

![alt text](https://github.com/disposetest1/project/blob/master/6_swagger.jpg)


**Consume the model endpoints**

- Here Information from the swagger documentation is used to consume the deployed model by executing the "endpoit.py" file that sends a POST HTTP request containing JSON DATA payload.

![alt text](https://github.com/disposetest1/project/blob/master/7_endpoint_output.jpg)


**Create publish and run pipeline**

- Here a pipeline for the model is created and ran with the result as seen below.

![alt text](https://github.com/disposetest1/project/blob/master/8_pipeline_created.jpg)

- The execution details can be seen under the "Use run details tab" of the Notebook.

![alt text](https://github.com/disposetest1/project/blob/master/12_run_details.jpg)


- The pipeline is also published, all this using the python SDK and  a JYUPITER playbook  which makes use of the bank marketing data set;

![alt text](https://github.com/disposetest1/project/blob/master/10_bankmarketing_dataset.jpg),

- Once the pipeline has been published, The pipeline endpoint is made available;

![alt text](https://github.com/disposetest1/project/blob/master/9_pipeline_endpoint.jpg),

- The published pipeline overview should be as seen below;

![alt text](https://github.com/disposetest1/project/blob/master/11_published_pipeline_overview.jpg),

- Move to pipeline to see further Scheduled/Completed runs;

![alt text](https://github.com/disposetest1/project/blob/master/13_scheduled_runs.jpg),



## Future Improvement. 
- Make use of Python SDK to train the models, build and run pipelines in a "write once use always" infrastructure as code way.
- To improve this project in the future, a deeper and more accurate experiment should be created to have better model results.

## Screen Recording
Here is a [Screen Recording](https://youtu.be/wbO601xOD90) for this project