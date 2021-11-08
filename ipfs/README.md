# liquidapps

## IPFS Service


Step-1

### Applying IPFS Manifest file to lauch new ipfs Pod

```
kubectl apply -f volume.yaml
kubectl apply -f deployment.yaml

````
Only thing to make sure here is the persistent disks. In this YAML file I have used Cloud Volumes. 
Depending upon your Setup.

Step-2

## Start service

```
kubectl apply -f deployment.yaml

```

