# Demo

- Webflux with spring security

```
- User : Guest

curl -X POST \
  http://localhost:8080/employees/update \
  -H 'authorization: Basic Z3Vlc3Q6cGFzc3dvcmQ=' \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{"id":"8","name":"Employee 8 UPDATE"}'
  
  Access Denied
  
```

```

- User : Admin

curl -X POST \
  http://localhost:8080/employees/update \
  -H 'cache-control: no-cache' \
  -H 'content-type: application/json' \
  -d '{"id":"8","name":"Employee 8 UPDATE"}'
  
  {"id":"8","name":"Employee 8 UPDATE"}
  
```


```
curl -X GET \
  http://localhost:8080/employees/ \
  -H 'cache-control: no-cache' \
  -H 'postman-token: 240ff650-aca2-2e49-ab86-1ce0c82edb32'
  
  [{"id":"1","name":"Employee 1"},{"id":"2","name":"Employee 2"},{"id":"3","name":"Employee 3"},{"id":"4","name":"Employee 4"},{"id":"5","name":"Employee 5"},{"id":"6","name":"Employee 6"},{"id":"7","name":"Employee 7"},{"id":"8","name":"Employee 8 UPDATE"},{"id":"9","name":"Employee 9"},{"id":"10","name":"Employee 10"}]
```