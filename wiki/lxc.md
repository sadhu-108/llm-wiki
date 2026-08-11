---
type: entity
created: 2026-08-11
updated: 2026-08-11
tags: [lxc, linux, containers]
sources:
  - raw/dhrpdocs-readthedocs-io-en-stable.pdf
---

# LXC (Linux Containers)

**LXC (Linux Containers)** is an operating-system-level virtualization method for running multiple isolated Linux systems on a single control host kernel.

## Role in Early Docker Architecture
In 2015, [[Docker]] relied directly on LXC as its underlying execution backend driver. Docker complemented LXC by adding process-level isolation, standard shipping-container abstractions, and image version control.
