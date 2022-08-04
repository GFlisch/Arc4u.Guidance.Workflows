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

