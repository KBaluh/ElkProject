# About project

It is template sample project how to logging with Serilog into Elastic Search and review with Kibana in docker containers

## Getting started

Install packages into project

```
Serilog.AspNetCore
Serilog.Enrichers.Environment
Serilog.Sinks.Elasticsearch
```

Pull images

```
docker pull docker.elastic.co/elasticsearch/elasticsearch:7.9.0
docker pull ocker.elastic.co/kibana/kibana:7.9.0
```

and prepare your docker-machine for elastic search

### Setup elastic search

https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html

### Install docker-machine

Before using from Windows install docker-machine
https://docs.docker.com/machine/install-machine/
with Git Bash

```bash
$ base=https://github.com/docker/machine/releases/download/v0.16.0 &&
  mkdir -p "$HOME/bin" &&
  curl -L $base/docker-machine-Windows-x86_64.exe > "$HOME/bin/docker-machine.exe" &&
  chmod +x "$HOME/bin/docker-machine.exe"
```

### Windows Docker Desktop
Then the `vm.max_map_count` setting must be set via docker-machine:

```cmd
docker-machine ssh
sudo sysctl -w vm.max_map_count=262144
```

### Windows Docker Desktop WSL 2

```cmd
wsl -d docker-desktop
sysctl -w vm.max_map_count=262144
```
