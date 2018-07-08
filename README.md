```
 _______           __ __                  
|   |   |.-----.--|  |__|.---.-.----.----.
|       ||  -__|  _  |  ||  _  |   _|   _|
|__|_|__||_____|_____|__||___._|__| |__|  

```

## What is Mediarr?

Mediarr is a set of Docker containers that run Plex, Radarr, Sonarr, Jackett, Rtorrent, Rutorrent and Nginx.


## Getting started

To start, make sure you have Docker installed and running with Linux containers by typing ```docker version``` in a terminal/cmd. Verify that ```OS/Arch``` is set to ```linux/amd64```, otherwise change this with your Docker agent.

Now, copy ```.env.example``` to ```.env``` and change accordingly.

If you're running Docker with Hyper-V, you may need to install VirtualBox to support the Docker Toolbox container. Please see [Docker prerequisite](https://docs.docker.com/machine/get-started/#prerequisite-information).

### Prerequisite

* Docker

## Installation
Installing Mediarr is pretty straight forward. Once you've got Docker installed, make and change a `.env` file and then run `docker-compose up`. Let's go thru it below, starting with codeonfiguration.

#### Configuration
Make a copy of `.env.example` to `.env`. Edit `.env` to suit your environment, especially the `MEDIA_PATH` part.


##### Start
Now you may start the Docker containers.
```
docker-compose up
```

If you rather have them run in background (daemonizing).
```
docker-compose up -d
```

##### Stop
Stop the Docker containers.
```
docker-compose down -d
```

#### Shell Access
Need to SSH into a container?
```
docker-compose exec <service> bash
```

## Services
Mediarr instances are available on the following endpoints.

| Name           | Reverse Proxy                     | Localhost               |
| -------------- | --------------------------------- | ----------------------- |
| nginx          | http://nginx.local                | http://localhost        |
| radarr         | http://radarr.local               | http://localhost:7878   |
| sonarr         | http://sonarr.local               | http://localhost:8989   |
| jackett        | http://jackett.local              | http://localhost:9117   |
| transmission   | http://transmission.local         | http://localhost:9091   |
| rutorrent      | http://rutorrent.local            | http://localhost:8080   |


#### Reverse Proxy
To access services using  Reverse Proxy address, add below rows to your operating system `hosts` file.
```
127.0.0.1	nginx.local
127.0.0.1	plex.local
127.0.0.1	sonarr.local
127.0.0.1	radarr.local
127.0.0.1	jackett.local
127.0.0.1	rutorrent.local
127.0.0.1	transmission.local
```

## Contribution
Feel free to create a [Pull Request](https://github.com/jeliasson/mediarr/pulls).

### Credits
Inspiration from
[ajohnsen](https://github.com/ajohnsen/plex-radarr-sonarr-transmission-openvpn-jackett-docker-compose)  and [hotio/docker-suitarr](https://github.com/hotio/docker-suitarr).
