# MERN Microservices deployment using AKS

This application has 3 microservices, 2 for the backend and 1 for the frontend.
```
tree --filelimits 3 MERN_Microservices_EKS_Deployment/
```
```
MERN_Microservices_EKS_Deployment/
├── README.md
├── backend
│   ├── README.md
│   ├── helloService  
│   └── profileService  
└── frontend 
```
## Table of Contents
1. [Set up the Azure Environment](#set-up-the-aws-environment)
   - 1.1 [Set Up Azure CLI](#set-up-aws-cli)
   - 1.2 [Create the Resource Group](#create-the-resource-group)
   - 1.3 [Create the Kubernetes Cluster](#create-the-kubernetes-cluster)
2. [Prepare the MERN Application](#prepare-the-mern-application)
   - 2.1 [Containerize the MERN Application](#containerize-the-mern-application)
   - 2.2 [Push Docker Images to Azure ACR](#push-docker-images-to-azure-acr)



## Set up the Azure Environment

### Set Up Azure CLI
Download and install the Azure CLI on Windows
```
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
```
After successful installation

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/7c32dfb6-1dcb-462a-a03f-b17e74c14510)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/85b452d5-3f26-497f-a432-dd371614139f)






### Creating the resource group
 - In the Azure Portal, click on “Create a resource” from the left-hand menu.
 - Search for “Resource group” and select “Resource group” from the results.
 - Click the “Create” button.
 - Enter a unique name for your resource group, such as “microservice_deployment”
 - Choose a region for the resource group (e.g., East US).
 - Click the “Review + Create” button and then click “Create” to create the resource group.

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/12ca557c-61e3-44e1-bb72-26bc8c54735e)



### Create the Kubernetes Cluster
 - In the Azure Portal, click on “Create a resource” again.
 - Search for “Kubernetes Service” and select “Kubernetes Service (AKS)” from the results.
 - Click the “Create” button to start the AKS creation wizard.


### Basics
 - In the “Basics” tab of the AKS creation wizard:
 - Choose your Azure subscription.
 - Select the resource group created before (“microservice_deployment”).
 - Enter a unique name for your AKS cluster (e.g., “Mern_Deployment”).
 - Choose the region for your AKS cluster (e.g., East US).
 - Select the desired Kubernetes version (e.g., 1.26.6).
 - For practice purposes and development/testing tasks, select a cluster preset configuration that suits your needs, such as “Dev/Test.”
 - This preset can provide you with predefined configurations optimized for these scenarios.
 - Specify the availability zones where your cluster nodes will be placed for increased resiliency.
 - AKS offers two pricing tiers for the managed Kubernetes control plane. Choose the pricing tier that best meets your needs.
 - Choose an upgrade type to determine when the cluster will be upgraded based on new AKS and Kubernetes releases. (For example, you can choose “Enable with Patch” for recommended automatic upgrades.)
 - For authentication and authorization, you can choose to use local accounts with Kubernetes RBAC. This provides a native Kubernetes RBAC managed locally within your AKS cluster.
 - Click “Next: Node Pools” to proceed.

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/f3827960-06d1-494f-9e65-f110a3fe2d23)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/14e6e73a-606f-45ac-a32f-38703a734892)

### Node Pool

 - You can add or customize node pools based on your application requirements.
 - Define the number of nodes, VM size, and other settings for your node pool.
 - Click “Next: Networking” when you’re ready to proceed.
   
![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/eef18acf-9a3b-499a-b6ec-58aefc1b5b53)

### Networking

 - Configure the networking settings for your AKS cluster. The default settings are usually sufficient for most use cases.
   
![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/a415b6ad-12ce-4191-b514-eda17071315d)

### Integration

 - Configure integrations with Azure services and features.
 - You can enable Azure Container Registry integration, Azure Policy, and more.

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/3843b7f1-7c59-412c-abd3-09650cec8333)

### Review + Create

 - Review all the configuration settings to ensure they are correct.
 - If everything looks good, click the “Create” button to start the provisioning of the AKS cluster.

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/939c1e93-12c7-4770-9aa3-6f9f1b970710)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/204db509-9fe2-4c4e-80a7-b8123c6cd0cd)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/37b2cc69-07c8-4c2b-b417-b3071ce380d4)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/c8076295-b35e-47c9-bdc2-c6f38c9d15a0)
















