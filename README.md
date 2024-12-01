# ELK_Docker
ElasticSearch Kibana Logstash using docker compose

# Docker compose 
docker-compose up 

open browers for following running services 

Elastic search
http://localhost:9200/

Logstash
http://localhost:9600/

Kibana
http://localhost:5601/

docker-compose down 

# Few docker commands
//force recreate containers
docker-compose up --force-recreate

//Get running container 
docker ps

//Open interactive session of container 
docker exec -it <ContainerId> sh

//exist interactive session of container
Exit(Ctl + p , Ctr + q)

//remove all the running containers 
docker rm (docker ps -aq) -f 

//filter the containers by name
docker ps --filter "name=elasticsearch" --filter "name=kibana" --filter "name=logstash"

//Get all running containers
docker ps all 

//get volume 
docker volume ls

//get network 
docker network ls

//remove volume by id
docker volume rm '<volumeId>'

//remove network by id 
docker network rm <NetworkId>
----------------
sample data available here https://www.kaggle.com/
----------
