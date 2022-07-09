## Running neo4j
### using docker


```bash
# regular
docker run -p7474:7474 -p7687:7687 -d --env NEO4J_AUTH=neo4j/test neo4j:latest

# apple silicon
docker run --platform linux/amd64 -p7474:7474 -p7687:7687 -d --env NEO4J_AUTH=neo4j/test neo4j:latest

# persisted
docker run -p7474:7474 -p7687:7687 -d \
        -v $HOME/neo4j/data:/data \
        -v $HOME/neo4j/logs:/logs \
        -v $HOME/neo4j/import:/var/lib/neo4j/import \
        -v $HOME/neo4j/plugins:/plugins \
        --env NEO4J_AUTH=neo4j/test neo4j:latest
```

then go to `http://localhost:7474/` with user as *neo4j* and pass as *test*.


