# Docker Ruby image for local development and CI purposes

## Building the container

1. clone repository

```
git clone https://github.com/redrick/ruby_base_image.git
```

2. jump into it

```
cd ruby_base_image
```

3. run docker build:

```
docker build -t redrick/ruby_base_image .
```

## Enter built container

You have to build it first :)

1. run container

```
docker run -it -d redrick/ruby_base_image
```

2. check out container ID

```
docker ps


CONTAINER ID        IMAGE                     COMMAND                  CREATED             STATUS              PORTS                     NAMES
7b8d99fc97d6        redrick/ruby_base_image   "bash"                   9 hours ago         Up 3 minutes                                  happy_dijkstra
```

3. run e.x. bash inside container (using container ID from above)

```
docker exec -it 7b8d99fc97d6 bash
```

4. run to kill the running container (also using container ID from above)

```
docker kill 7b8d99fc97d6
```
