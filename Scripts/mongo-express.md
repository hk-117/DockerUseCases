# Create Network mongo-net

```
docker network create mongo-net
```

# Run mongo container

```
docker run -d -p 27017:27017 \
-e MONGO_INITDB_ROOT_USERNAME=rootuser \
-e MONGO_INITDB_ROOT_PASSWORD=rootpass \
--name mongodb --net mongo-net mongo
```

# Run mongo-express container

```
docker run -d -p 8081:8081 \
-e ME_CONFIG_MONGODB_ADMINUSERNAME=rootuser \
-e ME_CONFIG_MONGODB_ADMINPASSWORD=rootpass \
-e ME_CONFIG_MONGODB_SERVER=mongodb \
--name mongo-express --net mongo-net mongo-express
```

# Access

```
http://localhost:8081
```
