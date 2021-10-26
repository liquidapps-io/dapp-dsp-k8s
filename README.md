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

