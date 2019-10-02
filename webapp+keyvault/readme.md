az group deployment create -g test --template-file webapp.json --parameters webapp.parameters.json

Pridat tvorbu key vaultu

create key vault

vytvorim secret - password
https://testtechtalkid.vault.azure.net/secrets/password/b21b48104a38440ba42bac11aec7e7f7

app service managed identity - system assigned

@Microsoft.KeyVault(SecretUri=https://testtechtalkid.vault.azure.net/secrets/password/b21b48104a38440ba42bac11aec7e7f7)

toto vyse dam do application settings

zkontroluji v console - env
a pak to bude v appsettings_password = Hodnota

