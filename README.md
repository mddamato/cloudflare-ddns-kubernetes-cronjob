# Pod-Cron-Job

## Overview

This chart is for deploying a cronjob in a namespace to perform periodic functions.

In addition to running a simple script input from the Values file it also includes the necessary service account setup to perform remote functions in other pods in the same namespace.

Reference <https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/> for more information on k8s cronjobs.

## Use case examples

- A postgres container is running in pod A. Cronjob, pod B, can start up once a day, exec into pod A, perform a `pgbackup` function, ship backup files, and then shut down.
- Run a test suite embedded in an image periodically.
- Run a quick health check script and report stats periodically.

## Install

`helm install files\kubernetes\pod-cron-job --name your-cronjob-name --namespace your-namespace-name --values your/values/file`
