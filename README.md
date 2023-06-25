# Pod-Cron-Job

## Overview

This chart is for deploying a cronjob in a namespace to perform periodic functions.

In addition to running a simple script input from the Values file it also includes the necessary service account setup to perform remote functions in other pods in the same namespace.

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