# Overview

This is a small Machine Learning App for Boston house price preiction based on a few parameters e.g. crime rate, distance to city centers etc. The app is implemented in python using scikit-learn and flask module. For running the application in the cloud azure web app Services is used. In this project you will find the code, the raw data for ML as well as the ML-model. Moreover we provide Makefile alonmg with Github actions and a YAML file to allow for CI/CD for further development and change in the code or input data. 

## Project Plan
<TODO: Project Plan

* https://trello.com/b/dzUvDvFY/udacity-dev-ops-proj2
* A link to a spreadsheet that includes the original and final project plan>

## Instructions

![ScreenShot](Deliverables/architecture.png {width=200px})

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

* Passing tests that are displayed after running the `make all` command from the `Makefile`

* Output of a test run

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

* Running Azure App Service from Azure Pipelines automatic deployment

* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application

> 

## Enhancements

<TODO: A short description of how to improve the project in the future>

## Demo 

<TODO: Add link Screencast on YouTube>


