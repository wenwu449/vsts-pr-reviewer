# vsts-pr-reviewer
A VSTS pull request review service, built on Azure Container Instance, Azure Logic App and Azure Service Bus.

#pr-image

# How it works
When a VSTS pull request is created or updated, VSTS sends a notification to an Azure Service Bus topic. As a subscriber of the topic, an Azure Logic App starts an Azure Container Instance upon getting the notification. The container in Azure Container Instance utilizes VSTS REST API to check the changes in the pull request, leave comments and vote approve/wait.

#flow-chart

# How to deploy

## deploy ARM template
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fwenwu449%2Fvsts-pr-reviewer%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fwenwu449%2Fvsts-pr-reviewer%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

## Auth ACI

## configure VSTS service hook

## get VSTS personal access token

## upload VSTS config

# Try it
