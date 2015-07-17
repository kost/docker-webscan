# k0st/alpine-nikto

Dockerized nikto

Image is based on the [gliderlabs/alpine](https://registry.hub.docker.com/u/gliderlabs/alpine/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/k0st/alpine-nikto.svg)](https://imagelayers.io/?images=k0st/alpine-nikto:latest 'latest')

## Docker image usage

```
docker run --rm -it k0st/alpine-nikto -host www.example.org -port 443 -ssl
```

## Examples

Run scan on https://www.example.org:

```
docker run --rm -it k0st/alpine-nikto -host www.example.org -port 443 -ssl
```

### Todo
- [ ] Check volume and data

