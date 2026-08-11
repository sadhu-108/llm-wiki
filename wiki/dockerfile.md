---
type: concept
created: 2026-08-11
updated: 2026-08-11
tags: [dockerfile, build, docker]
sources:
  - raw/dhrpdocs-readthedocs-io-en-stable.pdf
---

# Dockerfile

A **Dockerfile** is a text script containing sequential commands and instructions used by [[Docker]] to automate building a [[Docker Image]].

## Early Instruction Set (2015 Source)
* **`FROM <image>`**: Defines the base image to start the build process from. Must be the first instruction.
* **`RUN <command>`**: Executes shell commands inside the building layer and saves the result.
* **`INSERT <url> <path>`**: An early 2015 instruction used to download remote files directly into the image filesystem during builds.

> [!NOTE] Evolutionary Note
> The `INSERT` instruction featured in early 2015 documentation was later deprecated and replaced in modern Docker by `ADD` and `COPY`.
