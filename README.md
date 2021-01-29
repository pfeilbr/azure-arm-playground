# azure-arm-playground

```sh
RESOURCE_GROUP_NAME="armplayground01"

# create resource group
az group create --name "${RESOURCE_GROUP_NAME}" --location eastus

# deploy arm outputs example
az deployment group create \
    --name "my-deployment-01" --resource-group "${RESOURCE_GROUP_NAME}" \
    --template-file "templates/outputs.azuredeploy.json" \
    --parameters @templates/outputs.parameters.json

```