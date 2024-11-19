# How to use this project

1. Start the two containers using docker compose command 

`docker-compose up --build`

2. Access the web service via the load balancer:

Open a web browser and go to `http://localhost`.

3. Stop and Remove Containers

run `docker-compose down`

4. Remove all Docker build cache

run `docker-compose down --rmi all --volumes --remove-orphans`
