# liquidapps

## EOSIO Node

Step-1

Creating Configmap 


Use the kubectl create configmap command to create ConfigMaps. Before applying manifest update password in postgresql-cm.yaml

### Create the configmap

```
kubectl apply -f postgresql-cm.yaml

```

Step-2

### Applying Postgress Manifest file to lauch new postgress DB Pod

```
kubectl apply -f volumes.yaml
kubectl apply -f deployment.yaml

````
Only thing to make sure here is the persistent disks. In this YAML file I have used Cloud Volumes. 
Depending upon your Setup update volumes.yaml


Step-3

Start postgresql Service. Our service file is not exposed to internet. 

```
kubectl apply -f service.yaml

```
