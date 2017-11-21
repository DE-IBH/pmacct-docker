# Promiscuous mode traffic accountant

These are docker images for [pmacct](http://www.pmacct.net/) based on the offical Debian package.

## Tagged Docker Images

Images are tagged according to the installed pmacct version. The images are based on official Debain GNU/Linux releases.

### pmacct

* [`1.6.1`, `latest` Dockerfile](https://github.com/liske/pmacct-docker/blob/master/pmacct-1.6.1-debian/Dockerfile)

  [![Layers](https://images.microbadger.com/badges/image/liske/pmacct:1.6.1.svg)](https://images.microbadger.com/badges/image/liske/pmacct:1.6.1)
  This image is build using *Debian stretch* and should be considered **stable**.

## Usage

```
$ docker run --rm --net=host -v /path/to/confdir:/etc/pmacct:ro liske/pmacctd
```

```
# docker-compose.yml example
version: '3'
services:
  pmacct:
    image: liske/pmacct
    network_mode: host
    volumes:
      - ./conf/pmacct:/etc/pmacct:ro
    restart: always
```
