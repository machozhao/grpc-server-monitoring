# grpc-server-monitoring

## Run example
### Start greeting server
```
cd grpc-server-monitoring
go run greeter_server/main.go
```
### Run greeting client
```
cd grpc-server-monitoring
go run greeter_client/main.go
```
### Get prometheuse metrice
```
curl http://localhost:8080/metrics
```
### Start Prometheus server
```
docker run -p 9090:9090 -v /.../grpc-server-monitoring/prometheus/prometheus.yml:/etc/prometheus/prometheus.yml prom/prometheus
```
### Try to access Prometheus graph console

### Start Grafana and setup data source
```
docker run -d -p 3000:3000 grafana/grafana
```
Setup data source
```
Data source name: Prometheus
Data source type: Prometheus
Address: http://localhost:9090
Connect: Direct
```
### Import Grafana Data Exploration Dashboard
```
https://grafana.com/dashboards/456
```
