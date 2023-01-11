# Developer Sandbox Camel Labs

## Introduction

This repository contains a collection of labs to run in the Developer Sandbox, a free to use OpenShift environment, where users can follow guided instructions to fully cover the material in a fully remote development platform.

<br>

## Available labs

The table below collects the labs currently available and the articles in Red Hat Developers they're based on.

Follow the link to the article to run the lab you're interested in.

|            Lab Name             | Article | Preview in GitHub |
|:--------------------------------|:-------:|:-----------------:|
| Camel Spring Boot - Simple Demo | http:// | [preview](docs/labs/camelsb/walkthrough.adoc)
| Camel K = User Demo             | pending | [preview](docs/labs/camelk/walkthrough.adoc)

<br/>

## Contributing new labs

To include new labs to the collection, include the source code under a new folder and the documentation guide under `docs/labs` in a new folder.

You can test locally your guide instructions by running locally the Solution Explorer in a Docker instance using the following command:

```bash
docker run --rm -it --name solex -p 5001:5001 \
-v $PWD/docs/labs:/opt/user-walkthroughs \
-e NODE_ENV=production \
-e THREESCALE_WILDCARD_DOMAIN=local.localdomain \
-e OPENSHIFT_VERSION=4 \
-e WALKTHROUGH_LOCATIONS=/opt/user-walkthroughs quay.io/redhatintegration/tutorial-web-app:latest
```