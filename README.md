# rancher-prometheus
Simple Prometheus Stack Config for exposing [Rancher](https://www.rancher.com) API via [Prometheus](https://prometheus.io).

## Build Locally
```
docker build -t rancher-prometheus .
```

## Push
```
docker push REPO/rancher-prometheus
```

## Deploy to Rancher

Update `docker-compose.yml` to include your Docker Hub images, otherwise this will pull images that aren't your own.

```
rancher up --pull -d
```

## Services
- Prometheus - 9090
- prometheus-rancher-exporter - 9173
