# Rest-api-demo-with-springboot
A simple restful api implementation with spring boot and  persistence of entities using jpa/h2 in mem db

Import maven project and run app locally
  
### Using GUI to Create/Read/Update/Delete a user
Open Chrome - type :  http://localhost:5000/explorer/index.html#uri=/

View of  HAL browser to use APIs

![2021-10-11 17 29 31](https://user-images.githubusercontent.com/45326874/136857800-fa484ebd-b33d-4ca9-bcd9-2534899778cf.png)


### Using CURL to Create/Read/Update/Delete a user

From Command line/Terminal
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
