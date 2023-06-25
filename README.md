# cloudflare-ddns-kubernetes-cronjob

## Overview

Cronjob that checks records in cloudflare against public IP and updates if required 

Reference <https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/> for more information on k8s cronjobs.


## Install

```
helm upgrade --install cloudflare-ddns https://github.com/mddamato/cloudflare-ddns-kubernetes-cronjob/releases/download/0.6.0/cloudflare-ddns-kubernetes-cronjob-0.6.0.tgz --create-namespace --namespace cloudflare-ddns -f your_values.yaml
```

## Test

```
# install as usual from above instructions
# create temporary job from template of cronjob, to run immediately
kubectl create job --from=cronjob/cloudflare-ddns -n cloudflare-ddns manual-001
# check logs
kubectl logs -l job-name=manual-001 -n cloudflare-ddns
```

## publish

from working directory
```
helm package .
```