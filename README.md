# Simple Elastic Lab

## Docker
### Heap Size
- Update "ES_JAVA_OPTS" environment variable within Elasticsearch service "es01"
- 4GB heap size example: "ES_JAVA_OPTS=-Xms4g -Xmx4g"
- 2GB heap size example: "ES_JAVA_OPTS=-Xms2g -Xmx2g"

```
docker-compose up -d es01 
docker-compose exec es01 /bin/bash -c "bin/elasticsearch-setup-passwords auto --batch --url http://es01:9200"
```

- Update kibana credentials "ELASTICSEARCH_PASSWORD" in docker compose within Kibana service "kib01"

```
docker-compose up -d kib01
```


## URL
- Elasticsearch: http://localhost:9200/
- Kibana: http://localhost:5601/
