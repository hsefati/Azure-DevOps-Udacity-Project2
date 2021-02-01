## Overview

This is a small Machine Learning App for Boston house price preiction based on a few parameters e.g. crime rate, distance to city centers etc. The app is implemented in python using scikit-learn and flask module. For running the application in the cloud azure web app Services is used. In this project you will find the code, the raw data for ML as well as the ML-model. Moreover we provide Makefile alonmg with Github actions and a YAML file to allow for CI/CD for further development and change in the code or input data.

## Project Plan
The project plan comprises a general plan (see excel file) and a more detailed plan as a kanban board in Trello.  The Trello Board is used for daily stand-ups and adjust planning on daily basis.

* The kanban Board https://trello.com/b/dzUvDvFY/udacity-dev-ops-proj2

<img src="Deliverables/Screenshot%20Trello%20_%20Trello.png" width=500>

&nbsp;

* The Project plan in Excel: https://github.com/magnusse/Azure-DevOps-Udacity-Project2/blob/main/Deliverables/ProjectPlan.xlsx


## Instructions
This is an explanation of the general setup of the python app using sklearn and Flask. The architecture looks as follows:
<img src="Deliverables/architecture.png" width=600>

The python code along with the ML model, a Makefile and the Azure Pipeline configuration YAML-File you will find in the Github repository. The whole project can either be deployed as an Azure App Service using a CD pipeline in Azure DevOps or locally using your local machine or Azure Cloud Shell. Inn case of Azure App Service deployment the Machine Learning API (implemented in Python flask) is provided in the internet with a public IP address or the URL https://flaskmlservice.azurewebsites.net on port 443. In the latter case of local Test the Github repository is cloned to an Azure Cloud shell (or local bash) and the App is started with python. In that case the API can be used by "localhost" on port 5000.

In detail follow these steps get the App running on Azure App Services:

<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

* Project running on Azure App Service, please also read the official documentation of Microsoft https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops

  * Open a Cloud shell in Azure and clone or pull (if already cloned with earlier version) the repository https://github.com/magnusse/Azure-DevOps-Udacity-Project2.git
&nbsp;
  <img src="Deliverables/2021-01-24 21_49-screenshot-clones-repo.png" width=600>
&nbsp;
&nbsp;

  * Generate a webapp using Azure Cloud shell:
  ```bash
  udacity@Azure:~$ az webapp up -n flaskmlservice
  ```
  This will implement a template for an App which will be filled by the Azure Devops CD pipeline. Note: if you choose another name than _flaskmlservice_ you have to adapt this in the YAML file for Azure DevOps pipelines as well as in the .sh file for testing the application.

  * Go to Azure DevOps https://azure.microsoft.com/de-de/services/devops/start and create a new project, choose connection with Github (not Github enterprise) and connect with the repository https://github.com/magnusse/Azure-DevOps-Udacity-Project2.git .

  <img src="AzureDevops2021-02-01 09_10_22-New pipeline - Pipelines.png" width=600>
&nbsp;

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
