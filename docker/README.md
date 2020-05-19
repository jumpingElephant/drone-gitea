# CI: Gitea-Drone

This experiment uses Gitea and Drone to integrate a repository with CI

Tested with docker-compose only

## Prerequisites

Append to */etc/hosts*
```
127.0.0.1	drone
127.0.0.1	gitea
```

## Startup

Run Gitea: execute in gitea-directory
```
$ docker-compose up
```

Open settings Gitea to configure OAuth2 Application with redirect URI ```http://drone/login```

Copy Client-ID and Client Secret into *docker-compose.yml* in drone-directory

Run Drone: execute in drone-directory
```
$ docker-compose up
```

Configure upstream of this Git-Repository, push the sources and watch Drone building it.