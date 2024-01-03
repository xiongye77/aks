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
