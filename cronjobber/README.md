## Introduction

This chart creates and runs TZCronJob (CronJob with timezone support) inside Kubernetes.

## Installing the Chart

To install the chart with the release name `cronjobber`, run the following command:

```bash
$ helm repo add cronjobber https://github.com/hiddeco/cronjobber
$ helm install cronjobber/cronjobber --name cronjobber
```

## Uninstalling the Chart

To uninstall/delete the `cronjobber` deployment:

```bash
$ helm delete cronjobber
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

> **Tip**: To completely remove the release, run `helm delete --purge cronjobber`

## Configuration

The following table lists the configurable parameters of the Graphite chart and their default values.

|             Parameter          |            Description               |                  Default               |
|--------------------------------|--------------------------------------|----------------------------------------|
| `namespace`                    | Namespace                            | `default`                              |
| `image.cronjobber.repository`  | Docker image `cronjobber` repo       | `quay.io/hiddeco/cronjobber`           |
| `image.cronjobber.tag`         | Docker image `cronjobber` tag        | `0.2.0`                                |
| `image.updatetz.repository`    | Docker image `updatetz` repo         | `quay.io/hiddeco/cronjobber-updatetz`  |
| `image.updatetz.tag`           | Docker image `updatetz` tag          | `0.1.0`                                |
| `replicaCount`                 | Replica count                        | `1`                                    |


Specify each parameter using the `--set key=value[,key=value]` argument to `helm install`. For example:

```bash
$ helm install --name cronjobber --set namespace=cronjobs cronjobber/cronjobber
```

Alternatively, a YAML file that specifies the values for the parameters can be provided while installing the chart.
