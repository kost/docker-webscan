# k0st/debian-arachni

Docker Arachni Scanner container

Image is based on the [debian](https://registry.hub.docker.com/u/debian/) base image

## Docker image size

[![Latest](https://badge.imagelayers.io/k0st/debian-arachni.svg)](https://imagelayers.io/?images=k0st/debian-arachni:latest 'latest')

## Docker image usage

```
docker run k0st/debian-arachni 
```

## Default credentials

Consult https://github.com/Arachni/arachni-ui-web/wiki

Usually they are

**Administrator account**

E-mail: `admin@admin.admin`<br/>
Password: `administrator`

**Regular user account**

E-mail: `user@user.user`<br/>
Password: `regular_user`

## Examples

Run web UI:

```
docker run -p 9292:9292 k0st/debian-arachni
```

Run RPC service:
```
docker run --entrypoint=arachni_rpcd k0st/debian-arachni
```

Run console:
```
docker run --entrypoint=arachni_console k0st/debian-arachni
```



