```
 _______           __ __                  
|   |   |.-----.--|  |__|.---.-.----.----.
|       ||  -__|  _  |  ||  _  |   _|   _|
|__|_|__||_____|_____|__||___._|__| |__|  

```

## What is Mediarr?

Mediarr is a set of Docker containers that run Plex, Radarr, Sonarr, Jackett and Transmission.

## Getting started

To start, make sure you have Docker installed and running with Linux containers by typing ```docker version``` in a terminal/cmd. Verify that ```OS/Arch``` is set to ```linux/amd64```, otherwise .

Now, create a

If you're running Docker with Hyper-V, you may need to install VirtualBox to support the Docker Toolbox container. Please see [Docker prerequisite](https://docs.docker.com/machine/get-started/#prerequisite-information).

### Configuration

```

```

### Installation

```
docker-machine create box
```

#### Start

```
docker-machine create box
docker-compose up -d
```

#### Stop

```
docker-compose down -d
```

## Credits
Inspiration from
[ajohnsen](https://github.com/ajohnsen/plex-radarr-sonarr-transmission-openvpn-jackett-docker-compose)  and [hotio/docker-suitarr](https://github.com/hotio/docker-suitarr).

## Contribution
Feel free to create a Pull Request.
