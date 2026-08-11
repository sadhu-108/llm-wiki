---
type: concept
created: 2026-08-11
updated: 2026-08-11
tags: [docker-image, packaging, docker]
sources:
  - raw/dhrpdocs-readthedocs-io-en-stable.pdf
---

# Docker Image

A **Docker Image** is an immutable, read-only template used to instantiate a running [[Container]].

## Composition & Creation
* **Filesystem Template**: Contains application binaries, dependencies, configuration files, and initial environment specifications.
* **Build via Dockerfile**: Automated image generation is driven by a [[Dockerfile]].
* **Commit from Container**: Images can also be snapshotted from a modified container state using `docker commit`.
* **Repository Storage**: Images can be tagged and uploaded to or downloaded from a registry server (`docker pull`, `docker push`).
