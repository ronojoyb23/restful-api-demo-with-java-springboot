# restful-api-demo-with-springboot
a simple restful api with spring boot and  persistence of entities using jpa/h2 in mem db
do a maven import of the project and run application
to test use the following-
Open Chrome - type :  http://localhost:5000/explorer/index.html#uri=/
to access the HAL browser to use APIs using UI, POST API To create user, then any other CRUD API.
From the command line/terminal use-
### Create a user
Request:
```
curl -XPOST -H 'Content-Type: application/json' http://localhost:5000/user -d '{
  "first_name": "John",
  "last_name": "Doe",
  "client_name": "Company Inc."
}'
```
 
Response:
```
HTTP 200
{
  "id": 1,
  "first_name": "John",
  "last_name": "Doe",
  "client_name": "Company Inc."
}
```

### Fetch user by ID
Request:
```
curl -XGET http://localhost:5000/user/1
```

Response:
```
HTTP 200
{
  "id": 1,
  "first_name": "Human",
  "last_name": "Being",
  "client_name": "Company Inc."
}
```
### Delete user by ID
Request:
```
curl -XDELETE http://localhost:5000/user/1
```

Response:
```
HTTP 200
{}
```
