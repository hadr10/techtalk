# ARM Templates in TechTalk
## Introduction
Myself and info about me.

Why i choosed this topic?

## Azure quickstart templates

[Link to GitHub with Azure quickstart templates](https://github.com/Azure/azure-quickstart-templates)

and we will select for example 101-storage-account-create

[Create storage account](https://github.com/Azure/azure-quickstart-templates/tree/master/101-storage-account-create)

## How to deploy own templates
**Prerequisites**

[Azure CLI](https://docs.microsoft.com/cs-cz/cli/azure/install-azure-cli?view=azure-cli-latest)

1. Login to azure
    ```
    az login
    ```

2. Create resource group if you don't have
    ```
    az group create --name testaks --location southeastasia
    ```
3. Validate deployment
    ```
    az group deployment validate -g testaks --template-file storage.json --parameters storage-dev.parameters.json
    ```
4. Run deployment for dev
    ```
    az group deployment create -g testaks --template-file storage.json --parameters storage-dev.parameters.json
    ```
5. Run deployment for prod
    ```
    az group deployment create -g testaks2 --template-file storage.json --parameters storage-prod.parameters.json
    ```

## Where to store ARM Templates?
GitHub, GitLab

## Which tool use for writing?
Visual studio code

## Validation of ARM Template?
[How to validate ARM template](https://docs.microsoft.com/en-us/cli/azure/group/deployment?view=azure-cli-latest#az-group-deployment-validate)

## Azure button
<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fhadr10%2Ftechtalk%2Fmaster%2Fstorage.json" target="_blank">
<img src="http://azuredeploy.net/deploybutton.png"/>
</a>