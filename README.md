# OpenRCT2

An open-source re-implementation of RollerCoaster Tycoon 2. A construction and management simulation video game that simulates amusement park management.

This repository contains `Dockerfile` definitions for the command line version OpenRCT2. These images should be used for hosting multiplayer servers or executing commands such as generating screenshots.

You can pull and test the latest develop version by running:
```
$ docker run --rm openrct2/openrct2-cli:develop --version
```

## Multiplayer

To host a multiplayer server, create a container that exposes the desired port and pass in a URL to the park to load. For example:

```
$ docker run --rm -p 11753:11753 -it openrct2/openrct2-cli host https://bit.do/openrct2-bpb
```

All configuraion data is stored inside the container. If you want to persit it outside the container, you can mount it to a volume or your local filesystem. Mounting your local filesystem also allows you to read and write saved games locally. For example:

```
$ docker run --rm -p 11753:11753 -v /home/me/openrct2-config:/home/openrct2/.config/OpenRCT2 -it openrct2/openrct2-cli host /home/openrct2/.config/OpenRCT2/save/mypark.sv6
```

The command above will mount the OpenRCT2 user / config directory inside the container to a directory on your local filesystem. This will allow you to persist and edit the configuration, saved games etc. locally.

It will then host a new server and load the saved game `mypark.sv6` located in the mounted directory under the save sub-directory.

## Tags

v0.2.5 onwards are based on Ubuntu 20.04 (amd64). v0.2.4 and v0.2.3 use Ubuntu 19.04 (amd64), previous tags are based on Ubuntu 18.04 (amd64).

- [`develop` (*develop/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/develop/cli/Dockerfile)
- [`0.3.1`, `latest` (*0.3.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.1/cli/Dockerfile)
- [`0.3.0` (*0.3.0/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.0/cli/Dockerfile)
- [`0.2.6` (*0.2.6/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.6/cli/Dockerfile)
- [`0.2.5` (*0.2.5/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.5/cli/Dockerfile)
- [`0.2.4` (*0.2.4/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.4/cli/Dockerfile)
- [`0.2.3` (*0.2.3/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.3/cli/Dockerfile)
- [`0.2.2` (*0.2.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.2/cli/Dockerfile)
- [`0.2.1` (*0.2.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.1/cli/Dockerfile)
- [`0.2.0` (*0.2.0/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.0/cli/Dockerfile)
- [`0.1.2` (*0.1.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.1.2/cli/Dockerfile)
