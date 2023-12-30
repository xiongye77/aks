# aks

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




# Template
kubectl create secret docker-registry <secret-name> \
    --namespace <namespace> \
    --docker-server=<container-registry-name>.azurecr.io \
    --docker-username=<service-principal-ID> \
    --docker-password=<service-principal-password>

# Replace
kubectl create secret docker-registry acrdemo2ss-secret \
    --namespace default \
    --docker-server=acrdemo2ss.azurecr.io \
    --docker-username=80beacfe-7176-4ff5-ad22-dbb15528a9a8 \
    --docker-password=0zjUzGzSx3_.xi1SC40VcWkdVyl8Ml8QNj    

# List Secrets
kubectl get secrets    
