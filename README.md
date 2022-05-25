# golang mongodb start 




#  Document


## Install

https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/



##  create a user for mongodb

```shell

use admin  // ***  use admin database first


db.createUser(
  {
    user: "myUserAdmin",
    pwd: "abc123",
    roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
  }
)
```

##  import  dataset

###  json

```shell
https://www.mongodb.com/docs/atlas/sample-data/sample-mflix/#std-label-sample-mflix
```

**create dabase & collection then import dataset**
```shell

use sample_mflix;
db.createCollection("movies");
mongoimport --db sample_mflix --collection movies --file  ./movies.json

```

**query dataset**
```shell
db.movies.find( {"title" : "The Arrival of a Train"} );

```


###  import bson file
```shell
mongorestore -d sample_mflix   --dir  ./sample_mflix

sample_mflix dbname
./sample_mflix dir_name

```


## golang api
https://www.mongodb.com/docs/drivers/go/current/quick-start/




##  Others

```shell
db.things.stats();
```
