[![Docker Repository on Quay](https://quay.io/repository/alfresco/alfresco-base-java/status?token=7b035610-24b5-4ed7-a95f-6e812628cd8e "Docker Repository on Quay")](https://quay.io/repository/alfresco/alfresco-base-java)

# Welcome to Alfresco Docker Base Java

This repository contains the Dockerfile to create the base Java image that will be used by Alfresco engineering teams, other internal groups in the organisation, customers and partners to create images as part of the Alfresco Digital Business Platform.

The architectural decision record can be found [![here](https://img.shields.io/badge/Bamboo-PRIVATE-red.svg)](https://github.com/Alfresco/alfresco-anaxes-shipyard/blob/master/docs/adrs/0005-base-java-docker-image-composition.md).

# Versioning

Currently any pull request to this project should be accompanied by an increment to the `DOCKER_IMAGE_TAG` in `build.properties` as Bamboo will automatically build and push a new image to Quay.io.

# How to Build

To build a local version of the base java image follow the instructions below

1. Prepare the docker build environment. This will get the appropriate version of the Oracle Java Server JRE. Run the following script
```bash
./build-prep.sh
```

2. Build the docker image
```bash
docker build -t alfresco/alfresco-docker-base-java .
```