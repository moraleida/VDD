# varying-docker-dockers

VDD is an attempt at a VVV-inspired development environment for WordPress, minus the overhead of a Virtual Machine

# Requirements
Install [Docker], [Compose] and [nsenter]

## The First run


## Usage
```
docker-compose build
docker-compose up -d
docker-compose logs
docker-compose stop
docker-compose rm
```

## To use the command line
```
docker_exec -it vdd_base_1 /bin/bash
```

=====================

[Docker]:                      https://www.docker.io/
[Compose]:                     http://docs.docker.com/compose/install/
[nsenter]:                     https://github.com/jpetazzo/nsenter
