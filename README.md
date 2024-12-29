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

get all 

```
POST /ab_nyc_2019/_search
{
  "query" :{
    "match_all" : {
      
    }
  }
}

```


# Few docker commands
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

docker volume prune
```


links

https://www.kaggle.com/

https://www.elastic.co/guide/en/elasticsearch/client/net-api/current/getting-started-net.html

https://medium.com/@lucasgarciaz2018/using-elasticsearch-and-nest-in-net-9821f64cfa76

https://www.elastic.co/guide/en/elasticsearch/client/net-api/current/getting-started-net.html

https://www.tutorialspoint.com/elasticsearch/elasticsearch_cat_apis.htm


