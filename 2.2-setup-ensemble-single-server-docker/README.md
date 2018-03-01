# How To Use

This will start Zookeeper in replicated mode. Run following command,

```
docker stack deploy -c stack.yml zookeeper
```
or

```
docker-compose -f stack.yml up
```

# Check Zookeeper Status

To check run the following command

```
netstat -plntu
```

# Detect Zookeeper Leader & Follower

If zookeeper is run successfully then there will be one leader. To figure it
first list zookeeper container ID,

```
docker ps | awk {'print $1'}
```

Then run following command to detect follower/leader status,

```
docker exec -it CONTAINER_ID bash bin/zkServer.sh status
```
