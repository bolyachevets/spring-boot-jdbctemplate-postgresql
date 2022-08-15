## Create Tekton Pipelines
```
helm install java-crud-webhook . --values=examples/java-crud.yaml
```
## Tear down Tekton Pipelines
```
helm uninstall java-crud-webhook
```

## Create BuildConfigs
```
oc create -f build-configs/java-crud-bc.yaml
oc create -f build-configs/postgress-bc.yaml
```

## Deploy OpenShift YAMLs

```
oc create -f java-crud-bc.yaml
oc process -f db.yaml -p TAG=test | oc apply -f -
```
