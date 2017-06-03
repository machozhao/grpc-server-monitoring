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
![Setup datasource](https://github.com/machozhao/grpc-server-monitoring/blob/master/blob/grafana_setup_ds.png?raw=true)
### Import Grafana Data Exploration Dashboard
```
https://grafana.com/dashboards/456
```
![Access databoard](https://github.com/machozhao/grpc-server-monitoring/blob/master/blob/grafana_setup_ds.png)
