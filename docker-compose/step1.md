#### Let's pre-pull required images

```
docker-compose pull
```{{exec}}

<br>

#### Let's walkthrough docker-compose.yaml ----->


<br>

#### Let's run it:

```
docker-compose up -d
```{{exec}}

<br>

#### Check running containers:

```
docker-compose ps
```{{exec}}

<br>

#### Check container logs:

```
docker-compose logs mariadb
```{{exec}}

<br>

#### Access phpMyAdmin Web UI using this link:

[Open phpMyAdmin Web UI]({{TRAFFIC_HOST1_8080}})

<br>

#### Stop running containers:

```
docker-compose down
```{{exec}}

<br>

#### Check running containers:

```
docker-compose ps
```{{exec}}

<br>