# aws-inferentia-neuron-sdk-docker
Dockerfile and helper for AWS Inferentia [Neuron SDK](https://github.com/aws/aws-neuron-sdk) with utilities for `Tensorflow` and `Pytorch` models compilation.

## Build
We build the Docker container
```
docker build -f Dockerfile -t neuronsdk .
```

## Run
We run the Docker image as daemon with a attached `/src` volume for editable sources and a `/root` volumes for models files.
```
docker run --rm -it -d -v `pwd`/src:/app -v $VOLUME:/root --name neuronsdk-compile neuronsdk
docker exec -it neuronsdk-compile bash
```

## Docker images
The build Docker image is

```
REPOSITORY                         TAG                 IMAGE ID            CREATED             SIZE
neuronsdk                          latest              7cb529332e30        21 hours ago        7.63GB
```

