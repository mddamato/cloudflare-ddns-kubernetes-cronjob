# Pod-Cron-Job

## Overview

This chart is for deploying a cronjob in a namespace to perform periodic functions.

In addition to running a simple script input from the Values file it also includes the necessary service account setup to perform remote functions in other pods in the same namespace.

Reference <https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/> for more information on k8s cronjobs.


## Install

```
helm install https://github.com/mddamato/cloudflare-ddns-kubernetes-cronjob/blob/main/cloudflare-ddns-kubernetes-cronjob-0.1.0.tgz -f your_values.yaml
```

