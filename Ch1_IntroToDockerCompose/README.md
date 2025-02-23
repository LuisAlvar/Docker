### Normal NGINX image 
```batch
docker run --rm -p 8080:80 --name nginx-compose nginx
curl 127.0.0.1:8080
```


### NGINX image with custom index.html
```batch
docker run --rm -p 8080:80 --name nginx-compose -v $(pwd)/static-site:/usr/share/nginx/html nginx
curl localhost:8080/index.html
```

### NGINX image within a docker compose file 
Create the docker-compose.yaml file 
```batch
docker compose up
```
Within other terminal
```batch
docker ps
docker exec -it chp1_-nginx-1 cat /etc/nginx/nginx.conf
docker cp chp1_-nginx-1:/etc/nginx/nginx.conf nginx.conf
```

### Create a DockerFile for Custom NGINX 
```batch
docker build -t custom-nginx:0.1 .
```

