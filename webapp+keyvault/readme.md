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

Go to [website](https://techtalkidweb-webapp.azurewebsites.net/
)
vytvorim secret - password
https://techtalkidwebkeyvault.vault.azure.net/secrets/password/b21b48104a38440ba42bac11aec7e7f7

nastavit prava pro muj ucet

app service managed identity - system assigned

@Microsoft.KeyVault(SecretUri=https://testtechtalkid.vault.azure.net/secrets/password/b21b48104a38440ba42bac11aec7e7f7)

toto vyse dam do application settings

zkontroluji v console - env
a pak to bude v appsettings_password = Hodnota

