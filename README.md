# liquidapps

## EOSIO Node

Step-1

Creating Configmap 
Create config.ini file using [liquidapps-docs](https://docs.liquidapps.io/en/v2.0/dsps/eosio-node.html#configuration)


Use the kubectl create configmap command to create ConfigMaps

### Create the configmap
```
kubectl create configmap eos-config --from-file=config.ini
```

Step-2

### Applying EOS Manifest file to lauch new EOS Pod

```
kubectl apply -f deployment.yaml

````
Only thing to make sure here is the persistent disks. In this YAML file I have used Cloud EBS Volumes. 
Depending upon your Setup.
