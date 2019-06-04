# Promiscuous mode traffic accountant

These are docker images for [pmacct](http://www.pmacct.net/) based on the offical Debian package.

## Tagged Docker Images

Images are tagged according to the installed pmacct version. The images are based on official Debain GNU/Linux releases.

### pmacct

* [`1.z.2`, `latest` Dockerfile](https://github.com/DE-IBH/pmacct-docker/blob/master/pmacct-1.7.2-debian/Dockerfile)

  [![Layers](https://images.microbadger.com/badges/image/ibhde/pmacct:1.7.2.svg)](https://images.microbadger.com/badges/image/ibhde/pmacct:1.7.2)
  This image is build using *Debian buster* and should be considered **testing**.

* [`1.6.1`, `latest` Dockerfile](https://github.com/DE-IBH/pmacct-docker/blob/master/pmacct-1.6.1-debian/Dockerfile)

  [![Layers](https://images.microbadger.com/badges/image/ibhde/pmacct:1.6.1.svg)](https://images.microbadger.com/badges/image/ibhde/pmacct:1.6.1)
  This image is build using *Debian stretch* and should be considered **stable**.

## Usage

```
$ docker run --rm --net=host -v /path/to/confdir:/etc/pmacct:ro ibhde/pmacctd
```

```
# docker-compose.yml example
version: '3'
services:
  pmacct:
    image: ibhde/pmacct
    network_mode: host
    volumes:
      - ./conf/pmacct:/etc/pmacct:ro
    restart: always
```
