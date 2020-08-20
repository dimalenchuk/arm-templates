## Import Client Certificate via ARM Templates in API Management for Mutual Authentication

# Steps:
1. Put the Certificate in KeyVault /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.KeyVault/vaults/{vaultName}
2. Setup Certificate [Issuance Policy](https://docs.microsoft.com/en-us/azure/key-vault/certificates/about-certificates#certificate-policy) For Auto renew 
3. Use ARM Template Reference to fetch Certificate using [Static KeyVaultId](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/key-vault-parameter?tabs=azure-cli#reference-secrets-with-static-id)
4. Use the Arm Template createpim-mutualauthcert.json to update certificate into API Management


# Notes:
1. The [Authenticate-Certificate](https://docs.microsoft.com/en-us/azure/api-management/api-management-authentication-policies#ClientCertificate) policy needs to be updated
2. The Backend needs to be updated to switch to Subject Name + Issuer validation
3. If you are using the Certificate in the Backend Entity to authenticate to [Service Fabric Backend](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-tutorial-deploy-api-management#microsoftapimanagementservicebackends), then Backend entity needs to be updated
