# Overview

<TODO: complete this with an overview of your project>

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
https://trello.com/b/qShjinRh/udacity
* A link to a spreadsheet that includes the original and final project plan>
https://docs.google.com/spreadsheets/d/1adD7ddET7H6If_gSujR9LW9NcaNk3ki8Wul1RFtCxJY/edit#gid=1348135932

## Instructions
In this project, you will build a Github repository from scratch and create a scaffolding that will assist you in performing both Continuous Integration and Continuous Delivery. You'll use Github Actions along with a Makefile, requirements.txt and application code to perform an initial lint, test, and install cycle. Next, you'll integrate this project with Azure Pipelines to enable Continuous Delivery to Azure App Service.
<TODO:  
* Architectural Diagram (Shows how key parts of the system work)>

Instructions
Enter to Azure Portal with your Accoutn and open a Azure Cloud shell ( use Bash)
If you are not created one , just follow the first creation and wait a seconds to get your Cloud Shell.

First of all set up SSH Keys in your azure cloud shell, add the id_rsa.pub key to your GitHub repo ( ssh keys) and then clone the project there.
ssh-keygen -t rsa
 cat ~/.ssh/id_rsa.pub

Project Scaffolding ( files):
Plugin	README
Makefile	to create shortcuts to build, test, and deploy a project
requirements.txt	to list what packages a project needs
hello.py	a basic python app
test_hello.py	the test python file to above app
Create a virtual environment for your application.

python3 -m venv ~/.myrepo
source ~/.myrepo/bin/activate
Run make all which will install, lint, and test code
make all
Next set up Github Actions in your repo doign this :
just add an space on botton of file .github/workflows/pythonapp.yml and save it

ls -lasth .github/workflows/pythonapp.yml
vim .github/workflows/pythonapp.yml
Go to GItHUb Actions and you will see the Workflow in action!!!

Note: it was created a simple GitHUB Action in the branch which automates the lint and test of our app. Note: You can add the GitHub Actions badge to you README.md ( it's a good practice to do that)



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


[![Python application test with Github Actions](https://github.com/vanvietngo/Project-Scaffolding/actions/workflows/blank.yml/badge.svg)](https://github.com/vanvietngo/Project-Scaffolding/actions/workflows/blank.yml)