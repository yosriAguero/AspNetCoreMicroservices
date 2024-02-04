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