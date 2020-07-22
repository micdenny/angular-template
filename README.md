# Instruction

## Build image

### Blank image

```shell
docker build -t angular-template:9 ./9
docker build -t angular-template:10 ./10
docker build -t angular-template:latest ./latest
```

### Material image

```shell
docker build -t angular-template:9-material ./9/material
docker build -t angular-template:10-material ./10/material
```

## Run container

### Blank container

```shell
docker run -id --name angular-sample-9 angular-template:9
docker run -id --name angular-sample-10 angular-template:10
docker run -id --name angular-sample-latest angular-template:latest
```

### Material container

```shell
docker run -id --name angular-sample-9-material angular-template:9-material
docker run -id --name angular-sample-10-material angular-template:10-material
```

Then use the "Remote - Containers" extension of vscode to "Attach to running container"
