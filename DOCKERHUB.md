# Docker container for MKVToolNix
[![Docker Automated build](https://img.shields.io/docker/automated/jlesage/mkvtoolnix.svg)](https://hub.docker.com/r/jlesage/mkvtoolnix/) [![Docker Image](https://images.microbadger.com/badges/image/jlesage/mkvtoolnix.svg)](http://microbadger.com/#/images/jlesage/mkvtoolnix) [![Build Status](https://travis-ci.org/jlesage/docker-mkvtoolnix.svg?branch=master)](https://travis-ci.org/jlesage/docker-mkvtoolnix) [![GitHub Release](https://img.shields.io/github/release/jlesage/docker-mkvtoolnix.svg)](https://github.com/jlesage/docker-mkvtoolnix/releases/latest) [![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/JocelynLeSage/0usd)

This is a Docker container for [MKVToolNix](https://mkvtoolnix.download/).

The GUI of the application is accessed through a modern web browser (no installation or configuration needed on client side) or via any VNC client.

---

[![MKVToolNix logo](https://images.weserv.nl/?url=raw.githubusercontent.com/jlesage/docker-templates/master/jlesage/images/mkvtoolnix-icon.png&w=200)](https://mkvtoolnix.download/)[![MKVToolNix](https://dummyimage.com/400x110/ffffff/575757&text=MKVToolNix)](https://mkvtoolnix.download/)

MKVToolNix is a set of tools to create, alter and inspect [Matroska] files.

---

## Quick Start

**NOTE**: The Docker command provided in this quick start is given as an example
and parameters should be adjusted to your need.

Launch the MKVToolNix docker container with the following command:
```
docker run -d \
    --name=mkvtoolnix \
    -p 5800:5800 \
    -v /docker/appdata/mkvtoolnix:/config:rw \
    -v $HOME:/storage:rw \
    jlesage/mkvtoolnix
```

Where:
  - `/docker/appdata/mkvtoolnix`: This is where the application stores its configuration, log and any files needing persistency.
  - `$HOME`: This location contains files from your host that need to be accessible by the application.

Browse to `http://your-host-ip:5800` to access the MKVToolNix GUI.
Files from the host appear under the `/storage` folder in the container.

## Documentation

Full documentation is available at https://github.com/jlesage/docker-mkvtoolnix.

## Support or Contact

Having troubles with the container or have questions?  Please
[create a new issue].

For other great Dockerized applications, see https://jlesage.github.io/docker-apps.

[create a new issue]: https://github.com/jlesage/docker-mkvtoolnix/issues