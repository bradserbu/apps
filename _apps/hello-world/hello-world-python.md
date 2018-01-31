---
title:  "Hello World (python)"
date:   2017-09-15 12:00:00
author: Vanessa Sochat
tags: 
- ubuntu
- debian
- python
- scif
- singularity
files:
 - hello-world.py
 - py.scif
---

```yaml
%apprun hello-world-python
    exec python $SCIF_APPROOT/hello-world.py
%appfiles hello-world-python
    hello-world.py
%appinstall hello-world-python
    apt-get install -y python python-dev
```
