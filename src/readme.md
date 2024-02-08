Setup mongo docker 
use docker hub, docker pull mongo, 
docker run -d -p 27017:27017 --name shopping-mongo mongo
docker logs -f shopping-mongo
//it interactive terminal
docker exec it shopping-mongo /bin/bash 
mongosh
show dbs
use CatalogDb
db.createCollection('Products')
db.Products.insertMany([{ 'Name':'Asus Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':54.93 }, { 'Name':'HP Laptop','Category':'Computers', 'Summary':'Summary', 'Description':'Description', 'ImageFile':'ImageFile', 'Price':88.93 } ])

Why use repository ?
Abstraction between buisness layer and database context, mock to facilitate testing

Builder Mongo 
Helper class of type of document that contains method like filter and sort

What is the difference between docker compose and docker compose override?
one is for image definition and other for configuration (inect the app settings variable to override)

What is volume in docker 
data exists outside container and exists on the host

how to have clear docker ps -a ?
docker stop, docker rm

docker-compose -f .\docker-compose.yml -f .\docker-compose.override.yml up -d

