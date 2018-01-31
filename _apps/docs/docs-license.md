---
title:  "SCI-F License"
date:   2017-09-20 08:25:00
author: Vanessa Sochat
tags: 
- scif
- help
- linux
- singularity
---

```yaml

%apphelp docs-license

This module will add a LICENSE from a repo to a 
container, and then print it out fully for the user
when the app is run:

    scif run docs-license

    or in a container
 
    ./<container> run docs-license

%apprun docs-license
    cat ${SCIF_APPROOT}/LICENSE

%appfiles docs-license
    LICENSE*
```
