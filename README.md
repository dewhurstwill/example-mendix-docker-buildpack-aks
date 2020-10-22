# Example Mendix Docker Buildpack in Azure
An example of how to use the Mendix Docker Buildpack with Azure Kubernetes Service

## Prerequisites

* An Azure Subscription
* An Azure DevOps Project
* A public or private AKS cluster
* An Azure Container Registry
* An Azure FrontDoor or Traffic Manager pointing at the AKS cluster

## How-To

1. Fork this repo to your Azure DevOps Project
2. Upload your Mendix MDA file to the MendixApp folder
3. Configure a service connection for ACR (Azure Container Registry)
4. Configure a service connection for each kubernetes namespace
5. Configure a Pipeline Variable Group (Library) as outlined in _devops/Pipelines/azure-pipelines.yml
6. Import the pipeline (_devops/Pipelines/azure-pipelines.yml)
7. Apply all the kubernetes manifests except the deployment (this will be done by the pipeline)
8. Run the pipeline
