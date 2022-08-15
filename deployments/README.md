## Deploy OpenShift YAMLs

```
oc create -f java-crud-bc.yaml
oc process -f db.yaml -p TAG=test | oc apply -f -
```
