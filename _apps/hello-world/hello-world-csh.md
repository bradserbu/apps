---
title:  "Hello World (csh)"
date:   2017-09-15 12:00:00
author: Vanessa Sochat
tags: 
- scif
- singularity
- ubuntu
- debian
- csh
- shell
files:
 - hello-world.csh
 - csh.scif
---

```yaml
%apprun hello-world-csh
    exec csh $SCIF_APPROOT/hello-world.csh
%appfiles hello-world-csh
    hello-world.csh
%appinstall hello-world-csh
    apt-get install -y csh
```
