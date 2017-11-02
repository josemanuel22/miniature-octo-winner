# elasticsearch-metrics

https://grafana.net/dashboards/878

Run either as a standalone script or docker container.

To build the container:

```bash
git clone https://github.com/josemanuel22/fantastic-umbrella.git es-monitor
cd es-monitor
docker build -t es-monitor:latest .
```

To run it:

```bash
docker run -d -e ES_METRICS_CLUSTER_URL=http://134.171.189.10:9200 \
-e ES_METRICS_INDEX_NAME=elasticsearch_metrics-search1 \
-e ES_METRICS_MONITORING_CLUSTER_URL=http://134.171.189.10:9200 \
es-monitor:latest
```
