# ELK_Docker
ElasticSearch Kibana Logstash using docker compose


# To start the ELK stack on docker

```
docker-compose up

``` 

open browers for following running services 

Elastic search
http://localhost:9200/

Logstash
http://localhost:9600/

Kibana
http://localhost:5601/


# To stop the ELK stack in Docker.

```
docker-compose down

``` 

# Remove volume

By default, running 'docker-compose down' does not remove volumes. Remove the volume to avoid duplicate data from Logstash.

```
docker volume rm elk_docker_esdata

``` 
# Elastic search queries
You can open console in Kibana and run queries
```
POST /ab_nyc_2019/_search
{
  "query" :{
    "match_all" : {
      
    }
  }
}

POST /ab_nyc_2019/_search
{
  "query" :{
    "match_all" : {
    }
  },
  "_source": true
}

POST /ab_nyc_2019/_search
{
  "query" :{
   "match" : {
    "name" : "Beautiful Brooklyn Bedroom"
   }
  }
}

POST /ab_nyc_2019/_search
{
  "query" :{
    "match" : {
      "id" : "9859181"
    }
  }
}

GET /ab_nyc_2019/_doc/shQ1FJQBg2KQTfIbG1OP

```

# Docker commands
force recreate containers
```
docker-compose up --force-recreate

```

Get running container 
```
docker ps

```

Open interactive session of container 
```
docker exec -it <ContainerId> sh

```

Exist interactive session of container
```
Exit(Ctl + p , Ctr + q)

```

Remove all running containers 
```
docker rm (docker ps -aq) -f

``` 

Filter the containers by name
```
docker ps --filter "name=elasticsearch" --filter "name=kibana" --filter "name=logstash
```
Get all running containers

```
docker ps all 
```

Get volume 
```
docker volume ls
```

Get network 

```
docker network ls

```

Remove volume
```
docker volume rm '<volumeId>

```
https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data

