---
title:  "Hello World (clisp)"
date:   2017-09-15 12:00:00
author: Vanessa Sochat
tags: 
- ubuntu
- debian
- scif
- singularity
- clisp
files:
 - hello-world.clisp
 - clisp.scif
---

```yaml
%apprun hello-world-clisp
    exec clisp $SCIF_APPROOT/hello-world.clisp
%appfiles hello-world-clisp
    hello-world.clisp
%appinstall hello-world-clisp
    apt-get install -y clisp
```
