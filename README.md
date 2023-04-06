In one shell, run:  docker-compose up1
In another shell run 
```
curl "localhost:9200/_search?pretty" \
  -H 'Content-Type: application/json' \
  -d'{ "query": { "match_all": {} }}'
```

After making changes to the config to quickly rerun ES, run: `curl -X DELETE "localhost:9200/fluent-bit?pretty" && docker-compose restart fluent-bit`
