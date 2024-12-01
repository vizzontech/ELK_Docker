# ELK_Docker
ElasticSearch Kibana Logstash using docker compose

# Docker compose 
```docker-compose up``` 

open browers for following running services 

Elastic search
http://localhost:9200/

Logstash
http://localhost:9600/

Kibana
http://localhost:5601/

'''docker-compose down''' 

# Few docker commands
force recreate containers
```docker-compose up --force-recreate```

Get running container 
```docker ps```

Open interactive session of container 
```docker exec -it <ContainerId> sh```

Exist interactive session of container
```Exit(Ctl + p , Ctr + q)```

Remove all running containers 
```docker rm (docker ps -aq) -f``` 

Filter the containers by name
```docker ps --filter "name=elasticsearch" --filter "name=kibana" --filter "name=logstash"```

Get all running containers
```docker ps all ```

Get volume 
```docker volume ls```

Get network 
```docker network ls```

Remove volume by id
```docker volume rm '<volumeId>'```

Remove network by id 
```docker network rm NetworkId```
----------------
sample data available here https://www.kaggle.com/
----------
