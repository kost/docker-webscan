# k0st/alpine-dvcs-ripper

Dockerized dvcs-ripper from github 

Image is based on the [gliderlabs/alpine](https://registry.hub.docker.com/u/gliderlabs/alpine/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/k0st/alpine-dvcs-ripper.svg)](https://imagelayers.io/?images=k0st/alpine-dvcs-ripper:latest 'latest')

## Docker image usage

```
docker run --rm -it k0st/alpine-dvcs-ripper [rip-command] [options] -u [URL]
```

## Examples

Rip .git file from http://www.example.org/.git :
```
docker run --rm -it -v /path/to/host/work:/work:rw k0st/alpine-dvcs-ripper rip-git.pl -v -u http://www.example.org/.git 
```

Rip .hg file from http://www.example.org/.hg :
```
docker run --rm -it -v /path/to/host/work:/work:rw k0st/alpine-dvcs-ripper rip-hg.pl -v -u http://www.example.org/.hg 
```

### Todo
- [ ] Check volume and data

