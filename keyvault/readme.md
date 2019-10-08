# Key vault

1. Login to azure
    ```
    az login
    ```

2. Create resource group if you don't have
    ```
    az group create --name techtalkidkeyvault --location southeastasia
    ```
3. Validate deployment
    ```
    az group deployment validate -g techtalkidkeyvault --template-file keyvault.json --parameters keyvault.parameters.json
    ```
4. Run deployment
    ```
    az group deployment create -g techtalkidkeyvault --template-file keyvault.json --parameters keyvault.parameters.json
    ```

@Microsoft.KeyVault(SecretUri=https://testtechtalkid.vault.azure.net/secrets/password/b21b48104a38440ba42bac11aec7e7f7)
