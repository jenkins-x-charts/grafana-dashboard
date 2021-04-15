# Grafana Dashboard

This is a Helm Chart which contains Grafana dashboards, packaged in ConfigMaps.

This chart should be deployed alongside a Grafana chart, with the dashboards loader sidecar enabled, and the `label` configured to match.

If you want to add a dashboard, just create a new JSON file in the `dashboards` folder. Same if you want to remove/update a dashboard. The configmap template will automatically create as many configmaps as needed - which is 1 per dashboard.

## Dashboards

Name | Description | JSON file | Original Source
--- | --- | --- | ---
Cert-Manager | Displays [cert-manager](https://github.com/jetstack/cert-manager) logs & metrics, with certificates expiration dates | [cert-manager.json](dashboards/cert-manager.json) | N/A 
Cluster Overview | A quick overview of your Kubernetes cluster: nodes, pods, CPU/memory | [cluster.json](dashboards/cluster.json) | N/A 
Jenkins X | Default dashboard for the Jenkins X Grafana instances, listing all dashboards | [jenkins-x.json](dashboards/jenkins-x.json) | N/A 
Lighthouse | Displays [Lighthouse](https://github.com/jenkins-x/lighthouse) logs & metrics | [lighthouse.json](dashboards/lighthouse.json) | N/A 
Loki | Displays [Loki](https://github.com/grafana/loki) state | [loki.json](dashboards/loki.json) | [Grafana Dashboard #13407](https://grafana.com/grafana/dashboards/13407)
Prometheus | Displays [Prometheus](https://github.com/prometheus/prometheus) state | [prometheus.json](dashboards/prometheus.json) | [Grafana Prometheus datasource bundled dashboard](https://github.com/grafana/grafana/blob/master/public/app/plugins/datasource/prometheus/dashboards/prometheus_2_stats.json)
Tekton | Displays [Tekton](https://github.com/tektoncd/pipeline) logs & metrics | [tekton.json](dashboards/tekton.json) | N/A 
