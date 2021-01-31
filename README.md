µ# Overview

This is a small Machine Learning App for Boston house price preiction based on a few parameters e.g. crime rate, distance to city centers etc. The app is implemented in python using scikit-learn and flask module. For running the application in the cloud azure web app Services is used. In this project you will find the code, the raw data for ML as well as the ML-model. Moreover we provide Makefile alonmg with Github actions and a YAML file to allow for CI/CD for further development and change in the code or input data.

## Project Plan
<TODO: Project Plan

* The kanban Board https://trello.com/b/dzUvDvFY/udacity-dev-ops-proj2

![Screenshot](Deliverables/Screenshot%20Trello%20_%20Trello.png)
* The Project plan: https://github.com/magnusse/Azure-DevOps-Udacity-Project2/blob/main/Deliverables/ProjectPlan.xlsx


## Instructions
This is the general setup of the python app using sklearn and Flask.
![ScreenShot](Deliverables/architecture.png)


<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service

* Project cloned into Azure Cloud Shell

![Screenshot](Deliverables/2021-01-24%2021_28_50-screenshot-cloned-repo.png)

![Screenshot](Deliverables/2021-01-24%2021_49-screenshot-clones-repo.png)



* Passing tests that are displayed after running the `make all` command from the `Makefile`

![Screenshot](Deliverables/2021-01-24%2022_19_15-after-make-all.png)

* Output of a test run

![Screenshot](Deliverables/Azure-Shell-start-flask-locally2021-01-31%2021_31_32-.png)

![Screenshot](Deliverables/predict-local-My%20Dashboard%20-%20Microsoft%20Azure.png)


* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).

![Screenshot](Deliverables/2021-01-24%2022_43_39-github-action-testrun.png)


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
