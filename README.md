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

All configuration data is stored inside the container. If you want to persist it outside the container, you can mount it to a volume or your local filesystem. Mounting your local filesystem also allows you to read and write saved games locally. For example:

```
$ docker run --rm -p 11753:11753 -v /home/me/openrct2-config:/home/openrct2/.config/OpenRCT2 -it openrct2/openrct2-cli host /home/openrct2/.config/OpenRCT2/save/mypark.sv6
```

The command above will mount the OpenRCT2 user / config directory inside the container to a directory on your local filesystem. This will allow you to persist and edit the configuration, saved games etc. locally.

It will then host a new server and load the saved game `mypark.sv6` located in the mounted directory under the save subdirectory.

## Tags


| Tag version       | Ubuntu version |
|-------------------|----------------|
| v0.4.16+          | Ubuntu 24.04   |
| v0.4.11 - v0.4.15 | Ubuntu 22.04   |
| v0.2.5 - v0.4.10  | Ubuntu 20.04   |
| v0.2.3 - v0.2.4   | Ubuntu 19.04   |
| v0.1.2 - v0.2.2   | Ubuntu 18.04   |

All builds use the `amd64` architecture.

- [`develop` (*develop/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/develop/cli/Dockerfile)
- [`0.4.25`, `latest` (*0.4.25/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.25/cli/Dockerfile)
- [`0.4.24`, (*0.4.24/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.24/cli/Dockerfile)
- [`0.4.23`, (*0.4.23/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.23/cli/Dockerfile)
- [`0.4.22`, (*0.4.22/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.22/cli/Dockerfile)
- [`0.4.21`, (*0.4.21/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.21/cli/Dockerfile)
- [`0.4.20`, (*0.4.20/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.20/cli/Dockerfile)
- [`0.4.19.1` (*0.4.19.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.19.1/cli/Dockerfile)
- [`0.4.19`, (*0.4.19/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.19/cli/Dockerfile)
- [`0.4.18`, (*0.4.18/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.18/cli/Dockerfile)
- [`0.4.17`, (*0.4.17/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.17/cli/Dockerfile)
- [`0.4.16`, (*0.4.16/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.16/cli/Dockerfile)
- [`0.4.15`, (*0.4.15/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.15/cli/Dockerfile)
- [`0.4.14`, (*0.4.14/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.14/cli/Dockerfile)
- [`0.4.13`, (*0.4.13/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.13/cli/Dockerfile)
- [`0.4.12`, (*0.4.12/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.12/cli/Dockerfile)
- [`0.4.11`, (*0.4.11/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.11/cli/Dockerfile)
- [`0.4.10`, (*0.4.10/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.10/cli/Dockerfile)
- [`0.4.9`, (*0.4.9/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.9/cli/Dockerfile)
- [`0.4.8`, (*0.4.8/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.8/cli/Dockerfile)
- [`0.4.7`, (*0.4.7/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.7/cli/Dockerfile)
- [`0.4.6`, (*0.4.6/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.6/cli/Dockerfile)
- [`0.4.5`, (*0.4.5/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.5/cli/Dockerfile)
- [`0.4.4`, (*0.4.4/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.4/cli/Dockerfile)
- [`0.4.3`, (*0.4.3/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.3/cli/Dockerfile)
- [`0.4.2` (*0.4.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.2/cli/Dockerfile)
- [`0.4.1` (*0.4.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.1/cli/Dockerfile)
- [`0.4.0` (*0.4.0/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.4.0/cli/Dockerfile)
- [`0.3.5.1` (*0.3.5.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.5.1/cli/Dockerfile)
- [`0.3.5` (*0.3.5/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.5/cli/Dockerfile)
- [`0.3.4.1` (*0.3.4.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.4.1/cli/Dockerfile)
- [`0.3.4` (*0.3.4/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.4/cli/Dockerfile)
- [`0.3.3` (*0.3.3/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.3/cli/Dockerfile)
- [`0.3.2` (*0.3.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.2/cli/Dockerfile)
- [`0.3.1` (*0.3.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.1/cli/Dockerfile)
- [`0.3.0` (*0.3.0/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.3.0/cli/Dockerfile)
- [`0.2.6` (*0.2.6/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.6/cli/Dockerfile)
- [`0.2.5` (*0.2.5/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.5/cli/Dockerfile)
- [`0.2.4` (*0.2.4/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.4/cli/Dockerfile)
- [`0.2.3` (*0.2.3/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.3/cli/Dockerfile)
- [`0.2.2` (*0.2.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.2/cli/Dockerfile)
- [`0.2.1` (*0.2.1/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.1/cli/Dockerfile)
- [`0.2.0` (*0.2.0/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.2.0/cli/Dockerfile)
- [`0.1.2` (*0.1.2/cli/Dockerfile*)](https://github.com/OpenRCT2/openrct2-docker/blob/master/0.1.2/cli/Dockerfile)
