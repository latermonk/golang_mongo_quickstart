# golang mongodb start 


#  import  dataset
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

#  Document

##  create a user for mongodb
```shell
db.createUser(
  {
    user: "myUserAdmin",
    pwd: "abc123",
    roles: [ { role: "userAdminAnyDatabase", db: "admin" } ]
  }
)
```





----

```shell
db.things.stats();
```
