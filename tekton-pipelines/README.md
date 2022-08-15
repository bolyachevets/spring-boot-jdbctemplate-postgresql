## Create Tekton Pipelines
```
helm install java-crud-webhook . --values=examples/java-crud.yaml
```
## Tear down Tekton Pipelines
```
helm uninstall java-crud-webhook
```
## Deploy OpenShift YAMLs

e.g. DB:

```
oc process -f db.yaml -p TAG=test | oc apply -f -
```
