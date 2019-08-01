---
layout: post
title:  "Steps to create ci/cd for dotnet core projects"
date:   2019-07-30
categories: kubernetes
permalink: /category/kubernetes
---

> Steps to create ci/cd for dotnet core projects

This is a note for what needs to be done to create & upload & deploy a project into kubernetes cluster

## Prepare base images

- Prepare dotnet-core-runtime & dotnet-core-sdk base image. 
    modify corresponding `Dockerfile` in the git repo

- Upload base images to artifactory which is done via a jenkins job.

## Configure Jenkins to use this docker template.

![](/img/jenkins.jpg)

## Prepare your `CI` pipeline.

  - Need to have a step named something like `containerize` which is used to generate a docker image.
  - Need to have a step named something like `package` which is used to generate helm chart. 
    This will generate a chart which will be used for deploying 

## Prepare your `CD` pipeline.

  - `Optional` Create a base chart and upload it to corresponding git repo





