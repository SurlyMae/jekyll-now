---
layout: post
title: /Notes/ Containers
---

_Let's learn more about these, shall we?_

**Containers:**
- Creates a distributed application that leverages components in isolation
- Run on top of an engine (the Docker engine)
    - Docker is a standard AND a company; leader of the container ecosystem
- Approach software development differently
    - Are about structure and deployment, not about managing the application development process
- Have lower overhead for management and ops
- Are isolated, but can share OS and (where appropriate) bins/libraries
- When to use:
    - they do add cost and complexity (and initial latency in development)
    - to isolate apps for portability
    - to isolate apps for performance
    - to simplify development operations
    - to manage complexity
    - to leverage automation around portability/deployment
    - to provide better governance and security (by placing those services around the containers rather than within)
    - to provide better distributed computing capabilities
    - to provide automation services that can provide optimization and self-configuration
- Hold everything needed for an application to run, similar to a directory
- A container is an instance of an image
    - Images are read-only templates used to create Docker containers
- Registries are stateless, scalable, server-side apps that allow you to store and distribute Docker images (locally or not)
- Think of Docker Hub as GitHub for Docker container images (a central repo where you can store, maintain, retrieve Docker images)
- Data needs to be persisted in Docker for most apps, or the data won't exist after the container is shut down
    - Containers are short-term, and once a container is removed, the data is gone

From [Adrian Mouat](https://blog.container-solutions.com/understanding-volumes-docker)
- Docker file system works like this:
    - Docker images are stored as a series of read-only layers.
    - When a container is started up, Docker takes the read-only image and adds a read-write layer on top
    - if the container modifies an existing file, the file is copied out of the underlying read-only layer and into the top-most read-write layer where the changes are applied
    - The version in the read-write layer hides the underlying file, but doesn't destroy it; it still exists in the underlying layer. 
    - When a container is deleted, relaunching the image will start a fresh container without any of the changes made in the previously running container; those changes are lost.
    - Docker calls this combo of read-only layers w/ read-write layer on top a Union File System.
    - Docker data volumes are directories/files outside of the default Union File System and exist as normal directories/files on the host filesystem

[Cool guide to Kubernetes](https://azure.microsoft.com/en-us/resources/videos/the-illustrated-children-s-guide-to-kubernetes/)