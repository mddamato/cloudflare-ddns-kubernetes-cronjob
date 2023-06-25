# cloudflare-ddns-kubernetes-cronjob

## Overview

Cronjob that checks records in cloudflare against public IP and updates if required 

Reference <https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/> for more information on k8s cronjobs.


## Install

```
helm install cloudflare-ddns https://github.com/mddamato/cloudflare-ddns-kubernetes-cronjob/releases/download/0.1.0/cloudflare-ddns-kubernetes-cronjob-0.1.0.tgz --create-namespace --namespace cloudflare-ddns -f your_values.yaml
```

## publish

from working directory
```
helm package .
```