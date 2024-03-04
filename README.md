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
1. [Set Up the Azure Environment](#set-up-the-aws-environment)
   - 1.1 [Set Up Azure CLI](#set-up-aws-cli)
2. [Prepare the MERN Application](#prepare-the-mern-application)
   - 2.1 [Containerize the MERN Application](#containerize-the-mern-application)
   - 2.2 [Push Docker Images to Azure ACR](#push-docker-images-to-azure-acr)



## Set Up the Azure Environment

Download and install the Azure CLI in windows
```
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
```

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/85b452d5-3f26-497f-a432-dd371614139f)


![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/7c32dfb6-1dcb-462a-a03f-b17e74c14510)

creating the resource group
![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/12ca557c-61e3-44e1-bb72-26bc8c54735e)



Kubernetes cluster in AKS
![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/f3827960-06d1-494f-9e65-f110a3fe2d23)


![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/14e6e73a-606f-45ac-a32f-38703a734892)

Node Pool

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/eef18acf-9a3b-499a-b6ec-58aefc1b5b53)

Networking

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/a415b6ad-12ce-4191-b514-eda17071315d)

Integration

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/3843b7f1-7c59-412c-abd3-09650cec8333)

Review + Create

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/939c1e93-12c7-4770-9aa3-6f9f1b970710)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/204db509-9fe2-4c4e-80a7-b8123c6cd0cd)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/37b2cc69-07c8-4c2b-b417-b3071ce380d4)

![image](https://github.com/AdarshIITDH/MERN-deployment-on-AKS/assets/60352729/c8076295-b35e-47c9-bdc2-c6f38c9d15a0)
















