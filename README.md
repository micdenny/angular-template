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
docker build -t angular-template:latest-material ./latest/material
```

## Run container

### Blank container

```shell
docker run -id --name angular-sample-9 micdenny/angular-template:9
docker run -id --name angular-sample-10 micdenny/angular-template:10
docker run -id --name angular-sample-latest micdenny/angular-template:latest
```

### Material container

```shell
docker run -id --name angular-sample-9-material micdenny/angular-template:9-material
docker run -id --name angular-sample-10-material micdenny/angular-template:10-material
docker run -id --name angular-sample-latest-material micdenny/angular-template:latest-material
```

Then use the "Remote - Containers" extension of vscode to "Attach to running container"
