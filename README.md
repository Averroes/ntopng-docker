# ntopng-docker
[![](https://img.shields.io/docker/pulls/junquera/ntopng.svg?style=plastic)](https://hub.docker.com/r/junquera/ntopng)
![Docker Cloud Automated build](https://img.shields.io/docker/cloud/automated/junquera/ntopng.svg)
![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/junquera/ntopng.svg)

Docker for running [ntopng](https://github.com/ntop/ntopng)

## Build

```
docker build -t ntopng .
```

## Run

### After building from source

```
docker run --net=host -t -p 3000:3000 ntopng
```

### From docker hub...

```
docker run --net=host -t -p 3000:3000 junquera/ntopng
```

## Custom configuration

For adding aditional configuration there are two ways. First, by line arguments:

```
docker run --net=host -t -p 3000:3000 -e CONFIG=/ntop/ntopng.conf -v ./ntopng.conf:/ntop/ntopng.conf:ro junquera/ntopng
```

The other is through `docker-compose.yml` file.
