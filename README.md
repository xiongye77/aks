# AKS

![image](https://github.com/xiongye77/aks/assets/36766101/429d8d5d-aa6c-43d6-9b14-6c2f41b88dd0)


# Configure ACR integration for an existing AKS cluster
![image](https://github.com/xiongye77/aks/assets/36766101/1fc663dd-72d0-40ea-880e-5551eeacd41b)

Attach using acr-name
az aks update -n myAKSCluster -g myResourceGroup --attach-acr <acr-name>

Attach using acr-resource-id
az aks update -n myAKSCluster -g myResourceGroup --attach-acr <acr-resource-id>

# Detach an ACR from an AKS cluster

Detach using acr-name
az aks update -n myAKSCluster -g myResourceGroup --detach-acr <acr-name>

Detach using acr-resource-id
az aks update -n myAKSCluster -g myResourceGroup --detach-acr <acr-resource-id>


# Azure AKS Pull Docker Images from ACR using Service Principal
![image](https://github.com/xiongye77/aks/assets/36766101/ee8f2e15-f0b8-4595-852d-c9066fe5a29e)

Refer https://github.com/xiongye77/aks/blob/main/create-sp-access-acr-docker-secret.sh


![image](https://github.com/xiongye77/aks/assets/36766101/78c6dae5-2ee7-4bd7-a8de-c94161dd1d64)
![image](https://github.com/xiongye77/aks/assets/36766101/18e8e295-d60b-494e-8fea-fcc4d9a489f0)

# AKS upgrade 
![image](https://github.com/xiongye77/aks/assets/36766101/47876ec7-856c-4a45-817c-a20a444ee92d)




# Azure Virtual Node
Azure Kubernetes Virtual Nodes is a service offered by Microsoft Azure that allows Kubernetes cluster managers to deploy and manage their containerized workloads on a serverless infrastructure, without the need to manage and provision virtual machines.Azure Kubernetes virtual nodes work on an open-source Kubernetes Kubelet implementation called Virtual Kubelet. It is an open-source Kubernetes kubelet implementation that allows you to run your container workloads on various cloud providers, such as Azure Container Instances (ACI) and AWS Fargate.
![image](https://github.com/xiongye77/aks/assets/36766101/f641c882-491c-4167-9999-1fea60e015ae)
![image](https://github.com/xiongye77/aks/assets/36766101/6991ddab-2e2d-4ef4-b515-78aced371c61)



# Azure subscription not register resource provider

$AdminUserName = "labuser_74944_14531031@instructorwhizlabs.onmicrosoft.com"
$AdminPassword = "3tm$5?cKl9MUS*"
  
#Variable for Pscredential object
$SecurePassword = ConvertTo-SecureString $AdminPassword -AsPlainText -Force
$credentials = New-Object System.Management.Automation.PSCredential($AdminUserName, $SecurePassword)
   
#Connect to Azure Active Directory
Connect-AzAccount  –Credential $credentials
![image](https://github.com/xiongye77/aks/assets/36766101/51882aed-c045-417a-8bcd-495b66d3b2f9)
Connect-AzAccount 
Install-Module -Name Az -AllowClobber -Scope AllUsers -Force 
Get-AzResourceProvider -ListAvailable | Where-Object RegistrationState -eq "NotRegistered" | Select-Object ProviderNamespace, RegistrationState | Sort-Object ProviderNamespace
![image](https://github.com/xiongye77/aks/assets/36766101/c8d2301d-d71e-4838-b68e-7e0ef148a2d1)
