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

If zookeeper is run successfully then there will be one leader. To figure it out run the following command,

```
for i in `docker ps | awk {'print $1'} | tail -n +2`; do docker exec -it $i ./bin/zkServer.sh status | tail -n 1 ; done
```
