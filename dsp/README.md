# liquidapps

## DSP Node Setup

Step-1

Creating Configmap for config.toml. I have given example config.toml

You need more info refer here [liquidapps-docs](https://docs.liquidapps.io/en/v2.0/dsps/eosio-node.html#configuration)


Use the kubectl create configmap command to create ConfigMaps

### Create the configmap
```
kubectl create configmap dsp-config --from-file=config.toml

```

Step-2

### Applying EOS Manifest file to lauch new EOS Pod

```
kubectl apply -f volume.yaml
kubectl apply -f deployment.yaml

````
Only thing to make sure here is the persistent disks. In this YAML file I have used Cloud Volumes. 
Depending upon your cloud provider pls update and run Setup.

Step-3

### Running Service


```
kubectl apply -f service.yaml

````
