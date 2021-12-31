# Microservice-Architecture-ASP.NET-Core



mongo db 


docker run -d -p 27017:27017 --name shopping-mongo mongo

docker ps

docker logs -f shopping-mongo

docker exec -it shopping-mongo /bin/bash
ls
mongo
show dbs
use CatalogDb
db.createCollection('Products')
db.Products.insertMany([
    {
        "Name": "Asus Laptop",
        "Category":"Computers",
        "Summary":"Summary",
        "Description":"Description",
        "ImageFile":"ImageFile",
        "Price":54.93
    },
    {
        "Name": "HP Laptop",
        "Category":"Computers",
        "Summary":"Summary",
        "Description":"Description",
        "ImageFile":"ImageFile",
        "Price":88.93
    }
])
db.Products.find({}).pretty()
db.Products.remove({})
show databases
show collections
exit


docker ps -a
docker start <container-id-name>

docker ps -a

<!-- docker remove container  -->
docker rm <container-id>

docker images

docker ps -aq
docker stop $(docker ps -aq)
docker rmi $(docker images -q)
docker system prune

<!-- docker-compose -f docker-compose.yml -f docker-compose.override.yml up --build -->
docker-compose -f docker-compose.yml -f docker-compose.override.yml up -d
docker-compose -f docker-compose.yml -f docker-compose.override.yml down

----------------------------

redis

docker run -d -p 6379:6379 --name aspnetrun-redis redis

docker logs -f aspnetrun-redis

docker exec -it aspnetrun-redis /bin/bash
redis-cli

