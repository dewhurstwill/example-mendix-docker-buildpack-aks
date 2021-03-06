# Mendix Docker Buildpack in Azure
An example of how to use the [Mendix Docker Buildpack](https://github.com/mendix/docker-mendix-buildpack) with Azure Kubernetes Service

Disclaimer: This is not an official [Mendix](https://www.mendix.com/) product or documentation.
For more info regarding the docker buildpack, please visit https://github.com/mendix/docker-mendix-buildpack

## Prerequisites

* [An Azure Subscription](https://azure.microsoft.com/en-gb/free/)
* [An Azure DevOps Project](https://dev.azure.com)
* [A public or private AKS cluster](https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes)
* [An Azure Container Registry](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-intro)
* An [Azure FrontDoor](https://docs.microsoft.com/en-us/azure/frontdoor/front-door-overview) or [Traffic Manager](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview) pointing at the AKS cluster

## How-To
| Steps 📝 | 🛠 |
| - | - |
| Step 1. | Fork this repo to your Azure DevOps Project |
| Step 2. | Upload your Mendix MDA file to the MendixApp folder |
| Step 3. | Configure a service connection for ACR (Azure Container Registry) |
| Step 4. | Update the manifests to suit your deployment |
| Step 5. | Apply all the kubernetes manifests except the deployment (this will be done by the pipeline) |
| Step 6. | Configure a service connection for each kubernetes namespace |
| Step 7. | Configure a Pipeline Variable Group (Library) as outlined in _devops/Pipelines/azure-pipelines.yml |
| Step 8. | Import the pipeline (_devops/Pipelines/azure-pipelines.yml) |
| Step 9. | Run the pipeline |
