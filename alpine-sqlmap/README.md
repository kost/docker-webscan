# k0st/alpine-sqlmap-git

Dockerized sqlmap from github (git)

Image is based on the [gliderlabs/alpine](https://registry.hub.docker.com/u/gliderlabs/alpine/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/k0st/alpine-sqlmap-git.svg)](https://imagelayers.io/?images=k0st/alpine-sqlmap-git:latest 'latest')

## Docker image usage

```
docker run --rm -it k0st/alpine-sqlmap-git -u http://vuln.site.com/i?=1 -p i
```

## Examples

Run scan on https://www.example.org:

```
docker run --rm -it k0st/alpine-sqlmap-git -u http://vuln.site.com/i?=1 -p i
```

### Todo
- [ ] Check volume and data

