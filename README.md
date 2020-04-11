# Azure + Pulumi

This repository contains the dockerfile to create an image with [Pulumi](https://www.pulumi.com/) and the [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/?view=azure-cli-latest) installed

The main use for this is to ready-bake the installation so that we can run our Pulumi projects against Azure

Currently, this image is hosted on [Dockerhub]()

## Prerequisites

* [Docker](https://docs.docker.com/get-docker/)

## How to build image

```bash
docker build .
```

## Example of usage

Here's an example dockerfile that uses the image
```
FROM scottam/az-pulumi:latest

COPY . .

ENTRYPOINT["my-entrypoint.sh"]
```

## Exploring the contents of the image

Open it up! Take a look

```bash
docker run -it scottam/az-pulumi:latest bash
``` 