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