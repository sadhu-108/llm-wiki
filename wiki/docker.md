---
type: entity
created: 2026-08-11
updated: 2026-08-11
tags: [docker, container-runtime, linux]
sources:
  - raw/dhrpdocs-readthedocs-io-en-stable.pdf
---

# Docker

**Docker** is a Linux container platform designed to package, deploy, and run applications inside portable containers.

## Historical Architecture (2015 Source)
In its early 2015 architecture (Release 0), Docker served as a process-level management tool built on top of [[LXC]] (Linux Containers). Its primary innovation was standardizing software delivery using the shipping container metaphor:

* **Content-Agnostic**: Able to package any binary, library, code artifact, or database service regardless of language.
* **Infrastructure-Agnostic**: Able to run consistently across local development laptops, virtual machines, and cloud instances.

## Fundamental Components
* [[Docker Image]]: The read-only template containing application code and filesystem dependencies.
* [[Container]]: The isolated, executable instance created from an image.
* [[Dockerfile]]: The build blueprint specifying instructions to generate a Docker image.

## Historical Note on Operations
In early releases, the Docker daemon was executed manually via `docker -d`, and installation relied on distributions like Ubuntu 12.04 with LXC packages (`lxc-docker`). Modern Docker versions have replaced LXC with `containerd` and `runc`.
