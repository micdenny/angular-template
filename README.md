# Instruction

## Build image

```shell
docker build -t angular-template:9 ./9
docker build -t angular-template:10 ./10
docker build -t angular-template:latest ./latest
```

## Run container

```shell
docker run -id --name angular-sample-9 angular-template:9
docker run -id --name angular-sample-10 angular-template:10
docker run -id --name angular-sample-latest angular-template:latest
```

Then use the "Remote - Containers" extension of vscode to "Attach to running container"
