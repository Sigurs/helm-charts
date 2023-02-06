<!--- app-name: 5etools -->

# 5etools

5etools media server (check existing examples)

## TL;DR

```console
$ helm repo add sigurs https://sigurs.github.io/helm-charts
$ helm install my-release sigurs/5etools
```

## Introduction

Example of values.yaml that I I use: 

```yaml
ingress:
  hostname: <domain>

  # To enable TLS
  extraTls:
    - hosts:
       - <domain>
      secretName: <certificateSecret>

```
## Prerequisites

- Kubernetes 1.19+
- Helm 3.2.0+
- PV provisioner support in the underlying infrastructure
- ReadWriteMany volumes for deployment scaling

## Installing the Chart

To install the chart with the release name `my-release`:

```console
helm install my-release sigurs/5etools
```

The command deploys 5etools on the Kubernetes cluster in the default configuration. The [Parameters](#parameters) section lists the parameters that can be configured during installation.

> **Tip**: List all releases using `helm list`

## Uninstalling the Chart

To uninstall/delete the `my-release` deployment:

```console
helm delete my-release
```

The command removes all the Kubernetes components associated with the chart and deletes the release.

