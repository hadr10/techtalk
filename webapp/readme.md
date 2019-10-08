# Web application

1. Login to azure
    ```
    az login
    ```

2. Create resource group if you don't have
    ```
    az group create --name techtalkid --location southeastasia
    ```
3. Validate deployment
    ```
    az group deployment validate -g techtalkid --template-file webapp.json --parameters webapp.parameters.json
    ```
4. Run deployment
    ```
    az group deployment create -g techtalkid --template-file webapp.json --parameters webapp.parameters.json
    ```

Go to [website](https://techtalkidweb-webapp.azurewebsites.net/)

