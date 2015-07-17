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

Run scan on http://scanme.nmap.org:

```
docker run --rm -v /path/to/host/work:/work:rw k0st/alpine-skipfish -S /opt/skipfish/dictionaries/medium.wl -o /work/skipfish.out http://scanme.nmap.org
```


### Todo
- [ ] Check volume and data paths

