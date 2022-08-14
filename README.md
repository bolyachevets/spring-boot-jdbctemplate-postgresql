## Helm Chart
```
helm install java-crud-webhook . --values=examples/java-crud.yaml

helm uninstall java-crud-webhook
```

## Start Dev DB
```
docker compose -f docker-compose.yaml up
```

## Run Spring Boot application
```
mvn spring-boot:run
```

## Reachable at
http://localhost:8080/api/tutorials
