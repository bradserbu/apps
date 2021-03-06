---
title:  "workflow-internal-serial"
date:   2017-11-08 00:00:00
author: Bertrand Neron
files:
- workflow-internal-serial.scif
tags: 
- scif
- singularity
- workflow
- pipeline
- bash
- linux
---

```yaml
%applabels workflow-internal-serial
    MAINTAINER bneron@pasteur.fr

%apphelp workflow-internal-serial
    chain several app ('app_1' 'app_2' 'app_3' 'app_4') in series, behind each other.
    
%apprun workflow-internal-serial
    workflow=( 'app_1' 'app_2' 'app_3' 'app_4' )
    
    for step in "${workflow[@]}"
    do
        echo -e "\n##################################"
        echo "  Entering in step: ${step}"
        echo -e "##################################\n"
        export SINGULARITY_APPNAME=${step}
        /bin/bash /.singularity.d/actions/run
        status=$?
        if [ $status -ne 0]; then
            echo "ERROR : The step ${step} finished with non zero value ${status}"
            echo "ERROR : Stop the workflow"
            exit ${status}
        fi
    done
```
