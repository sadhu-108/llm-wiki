---
type: concept
created: 2026-08-11
updated: 2026-08-11
tags: [container, virtualization, docker]
sources:
  - raw/dhrpdocs-readthedocs-io-en-stable.pdf
---

# Container

A **Container** is an isolated runtime environment that executes software applications at the operating system process level.

## Key Characteristics
* **Lightweight Isolation**: Unlike virtual machines (which virtualize entire hardware stacks), containers isolate process namespaces, file systems, and network interfaces on the host kernel.
* **Instance of an Image**: A container is a running or stopped instance derived from a [[Docker Image]].
* **Standard Operations**: Standard containers support unified lifecycle operations such as start, stop, snapshot, commit, attach standard streams, and inspect.

## Contrast with Virtual Machines
| Aspect | Virtual Machine (VM) | Container |
| :--- | :--- | :--- |
| **Virtualization Level** | Hardware / Guest OS | Operating System / Process |
| **Resource Footprint** | Heavy (gigabytes, full OS) | Lightweight (megabytes, process-scoped) |
| **Primary Use Case** | Chunks of hardware allocation | Unit of software delivery |
