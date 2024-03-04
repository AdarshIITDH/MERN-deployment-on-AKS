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
