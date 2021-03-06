# docker-registry-viewer

A simple docker registry web manager

------------------------------------

### install

```
go get -u github.com/mkdym/docker-registry-viewer
```

### usage

```
export REGISTRY_HOST=127.0.0.1
export REGISTRY_PORT=5000
export REGISTRY_SSL=off
export LISTEN_PORT=49110
# need folder: resources
/path/to/docker-registry-viewer
```

### docker-build

```
# need sudo
# see script for image name
./docker-build.sh
```

### docker-usage

```
docker run -d --restart=always \
	--name docker-registry-viewer \
	-e REGISTRY_HOST=127.0.0.1 \
	-e REGISTRY_PORT=5000 \
	-e REGISTRY_SSL=off \
	-e LISTEN_PORT=49110 \
	-p 49110:49110 \
	mkdym/docker-registry-viewer
```

### cmd-tool

also provide a cmd tool, run `cmd-build.sh` to build, you will see it as `cmd-bin/regtool`

### screenshots

![homepage](readme-img/home.png)

