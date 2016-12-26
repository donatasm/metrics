# Grafana and Graphite in containers

To start:

```
docker-compose up -d
```

Access Grafana in a browser:

```
open http://$(docker-machine ip default):3000
```

Feeding data into Graphite:

```
echo "local.random.diceroll 4 `date +%s`" | nc -c $(docker-machine ip default) 2003
```
