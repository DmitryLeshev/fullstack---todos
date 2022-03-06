# To delete all containers including its volumes use,

- docker rm -vf $(docker ps -aq)

# To delete all the images,

- docker rmi -f $(docker images -aq)

# Commands

- START-DOCKER: docker-compose up -d
- START-DOCKER-DB: docker-compose up -d db
- START-DOCKER_v2: docker-compose --compatibility up
- CHECK-DOCKER: docker ps
- STOP-DOCKER: docker stop {{id_docker}}
- MIGRATION-POSTGRES: psql -h 127.0.0.1 -p 5432 -U USER DB < database.sql
- CONNECT-POSTGRES: psql -h 127.0.0.1 -p 5432 -U USER DB
- CHECK-TABLE-POSTGRES: \d
- SELECT-POSTGRES: SELECT \* FROM todo_item;
- EXIT-POSTGRES: \q

- ab -n 100000 -k -c 30 -q http://127.0.0.1:5000/