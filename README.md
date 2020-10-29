

Operationalizing Machine Learning Project:

This project was all about deploying ML models using Azure Platform. We learnt to deploy, authenticate, create and check logs, and use the deployed model as the REST API.


## Architectural Diagram
![alt text](./Screenshots/architectural_diagram.png)

Ways to improve:
1. Traini AutoML for longer duration to test out more models
2. Provide a good and custom cross validation strategy.

## Screen Recording
Kindly check the screen recording on [Youtube](https://www.youtube.com/watch?v=33qlU9rH50s)


## Key Steps

1. Dataset upload
The dataset on which we want to run AutoML is loaded in Azure ML studio.

![alt text](./Screenshots/0_dataset.png)

2. Experiment completed using Auto ML

Auto ML finds the best model as Voting Ensemble with AUC around 94%.

![alt text](./Screenshots/2_automl_completed.png)
![alt text](./Screenshots/3_best_model_run.png)
![alt text](./Screenshots/4_best_model_explanation.png)


3. Deployment of Best Model

In Azure, when we use ACI for deployment , we get a unique REST endpoint, SWAGGER URI and key. REST endpoint and key are used for authentication.

![alt text](./Screenshots/5_deploy_best_model_1.png)
![alt text](./Screenshots/6_deploy_best_model_2.png)
![alt text](./Screenshots/7_deploy_best_model_3.png)
![alt text](./Screenshots/8_model_list.png)
![alt text](./Screenshots/9_best_model_deployed.png)


4. Enable Logging

Logging enables us to find and debug errors.

![alt text](./Screenshots/11_logs.png)
![alt text](./Screenshots/12_logs_2.png)
![alt text](./Screenshots/13_application_insights.png)
![alt text](./Screenshots/14_application_insights_2.png)


5. Consume Model Endpoints

Swagger helps us identify and understand request and response parameters. It specifies GET and POST methods of REST API in our case.

We get a json response using REST URI and key for authentication.

![alt text](./Screenshots/15_swagger.png)
![alt text](./Screenshots/10_consume_best_model.png)
![alt text](./Screenshots/16_swagger_model.png)
![alt text](./Screenshots/17_swagger_model_2.png)
![alt text](./Screenshots/18_swagger_model_explanation.png	)
![alt text](./Screenshots/18_swagger_model_explanation_2.png)
![alt text](./Screenshots/19_endpoint_running.png)
![alt text](./Screenshots/20_endpoint_running.png)


6. Create and publish pipeline

In this step we use Azure ML Python SDK to create and publish a pipeline endpoint.

![alt text](./Screenshots/21_pipelines_running.png)
![alt text](./Screenshots/22_pipeline_active.png)
![alt text](./Screenshots/1_dataset.png)
![alt text](./Screenshots/22_jupyter_screenshot.png)