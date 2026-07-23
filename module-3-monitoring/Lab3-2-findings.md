# Lab 3.2 Findings

## Prometheus vs Grafana vs SigNoz

### Prometheus
- Open-source monitoring and alerting system.
- Collects metrics using a pull-based model.
- Uses PromQL for querying time-series data.
- Commonly used for infrastructure and Kubernetes monitoring.

### Grafana
- Visualization and dashboard platform.
- Connects to Prometheus as a data source.
- Displays metrics using graphs, gauges, and tables.
- Supports alerting based on metric thresholds.

### SigNoz
- Open-source observability platform.
- Supports metrics, logs, traces, and application performance monitoring (APM).
- Built on OpenTelemetry.
- Provides an integrated observability solution.

## Comparison

| Feature | Prometheus + Grafana | SigNoz |
|--------|-----------------------|---------|
| Metrics | Yes | Yes |
| Dashboards | Grafana | Built-in |
| Alerting | Yes | Yes |
| Logs | External tools required | Built-in |
| Distributed Tracing | External tools required | Built-in |
| OpenTelemetry | Partial | Native |
| Best Use Case | Infrastructure Monitoring | Full Observability |

## Conclusion

Prometheus and Grafana are ideal for infrastructure monitoring and visualization. SigNoz extends observability by combining metrics, logs, traces, and APM into a single platform, making it more suitable for cloud-native and distributed applications.
- Visualization and dashboard platform.
- Connects to Prometheus as a data source.
- Displays metrics using graphs, gauges, and tables.
- Supports alerting based on metric thresholds.

### SigNoz
- Open-source observability platform.
- Supports metrics, logs, traces, and application performance monitoring (APM).
- Built on OpenTelemetry.
- Provides an integrated observability solution.

## Comparison

| Feature | Prometheus + Grafana | SigNoz |
|--------|-----------------------|---------|
| Metrics | Yes | Yes |
| Dashboards | Grafana | Built-in |
| Alerting | Yes | Yes |
| Logs | External tools required | Built-in |
| Distributed Tracing | External tools required | Built-in |
| OpenTelemetry | Partial | Native |
| Best Use Case | Infrastructure Monitoring | Full Observability |

## Conclusion

Prometheus and Grafana are ideal for infrastructure monitoring and visualization. SigNoz extends observability by combining metrics, logs, traces, and APM into a single platform, making it more suitable for cloud-native and distributed applications.
