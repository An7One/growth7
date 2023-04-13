## Section 4 Logging & Monitoring

### Monitor Cluster Components

- Metrics Server
- Prometheus
- Elastic Stack
- DataDog
- dynatrace

```
> kubectl top node

// to identify the node that consumes the most CPU
> kubectl top node --sort-by='cpu' --no-headers | head -1

// to identify the pod that consumes the most memory
> kubectl top pod --sort-by='memory' --no-headers | head -1

// to identify the pod that consumes the least CPU
> kubectl top pod --sort-by='memory' --no-headers | tail -1
```

### Managing Application Logs

```
> kubectl logs -f event-simulator-pod

> kubectl logs -f event-simulator-pod event-simulator

> kubectl logs webapp-1
> kubectl logs webapp-2 -c simple-webapp
```
