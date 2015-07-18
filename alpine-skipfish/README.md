# k0st/alpine-skipfish

Dockerized skipfish

Image is based on the [gliderlabs/alpine](https://registry.hub.docker.com/u/gliderlabs/alpine/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/k0st/alpine-skipfish.svg)](https://imagelayers.io/?images=k0st/alpine-skipfish:latest 'latest')

## Docker image usage

```
docker run k0st/alpine-skipfish [skipfish option] [skipfish option] ...
```

## Examples

Run scan on http://127.0.0.1:

```
docker run --rm -v /path/to/host/work:/work:rw k0st/alpine-skipfish -S /opt/skipfish/dictionaries/medium.wl -o /work/skipfish.out http://127.0.0.1
```

Run scan on http://192.168.1.1 with minimal dict:
```
docker run -it --rm -v /data/work/work:/work:rw k0st/alpine-skipfish -o /work/192 -S /opt/skipfish/dictionaries/minimal.wl http://192.168.1.1
```


### Todo
- [ ] Check volume and data paths

