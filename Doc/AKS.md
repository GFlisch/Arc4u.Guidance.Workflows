# Azure Kubernetes Service

AKS.yml is the github workflow that will deploy an Arc4u micro-service to kubernetes.  
The workflow will:  
- Log into the Container registry
- Log into Azure for K8s.
- Select the resource group and the K8s cluster defined for the specific subscription (selected during the login step)
- Create the namespace if it doesn't exist.
- Delete the configmap if exist and create a new one with the configs based on the selected environment => see later.
- Prepare the deployment file
- Deploy to K8s.

## Secrets.

    ACR_User: The user of the azure container registry.
    ACR_Password: The password of the azure container registry.
    AZURE_CLIENT_ID:  The application id of the app registration.
    AZURE_CLIENT_SECRET:  The scret of the client.
    AZURE_TENANT_ID: The Tenant id where the k8s is hosted.
    AZURE_SUBSCRIPTION_ID: The subscription id where the k8s is hosted. 

    PS: The app registration will be at the level of the subscription, may be only at the level of the AKS is sufficient, assigned as a Contributor Role in the Role Assignments tab of the IAM Access control.