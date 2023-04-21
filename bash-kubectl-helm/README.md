# Bash - Helm - Kubectl
- This container contains bash, helm and kubectl components

# Getting Started
1. Build the docker image using [Dockerfile](./Dockerfile)
```shell
docker build -t bash-helm-kubectl:test .
docker images
```
2. Test kubectl version
```shell
docker run -it bash-helm-kubectl:test kubectl version
```
3. Test helm version
```shell
docker run -it bash-helm-kubectl:test helm version
```
3. Test bash shell
```shell
docker run -it bash-helm-kubectl:test bash
exit
```