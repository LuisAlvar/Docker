# Introduction to Docker Compose
- Create folder `static-site`
- Create `index.html` file with `static-site` folder
- Create `docker-compose.yaml` 
- While `docker compose up` run the following command to cp a file out of the container to local machine `docker cp chp1_-nginx-1:/etc/nginx/nginx.conf nginx.conf`
- Edit `nginx.conf` add escape=json
- Create `Dockerfile`
- Run `docker build -t custom-nginx:0.1 .`
- Edit `docker-compose.yaml` to use the new custom image of nginx
