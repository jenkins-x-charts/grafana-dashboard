# Jenkins X Grafana Dashboards Helm Chart

This repository contains a [Helm](https://helm.sh/) chart: [grafana-dashboard](charts/grafana-dashboard).

## Installation

### With Helm v3

```
$ helm repo add jx3 https://storage.googleapis.com/jenkinsxio/charts/
$ helm install grafana-dashboard jx3/grafana-dashboard
```

### With Helm v2

```
$ helm repo add jx3 https://storage.googleapis.com/jenkinsxio/charts/
$ helm repo update
$ helm install --name grafana-dashboard jx3/grafana-dashboard
```

## Configuration

See the [values.yaml](charts/grafana-dashboard/values.yaml) file for the configuration.
