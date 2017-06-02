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
