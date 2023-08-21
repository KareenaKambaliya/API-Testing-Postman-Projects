
# API-Testing-Postman-Projects

    The RESTful Booker CRUD Web API is a comprehensive and versatile tool designed for managing various operations on a booking system. This API allows you to Create, Read, Update, and Delete booking information through well-defined endpoints.
    
    A noteworthy resource that aligns perfectly with your goals is the "API-Testing-Postman-Projects" repository on GitHub. This repository likely contains practical examples, documentation, and possibly even pre-built Postman projects that demonstrate how to interact with the RESTful Booker API efficiently.




## Authors

- [@Kareena Kambaliya](https://github.com/KareenaKambaliya?tab=repositories)


# API Reference


## Authentication :
### Auth - CreateToken

```cURL
  curl -X POST \
  https://restful-booker.herokuapp.com/auth \
  -H 'Content-Type: application/json' \
  -d '{
    "username" : "admin",
    "password" : "password123"
}'
```
## Booking :

### Booking - GetBookingIds


```cURL
 curl -i https://restful-booker.herokuapp.com/booking
```


### Booking - Booking - GetBooking


```cURL
 curl -i https://restful-booker.herokuapp.com/booking/315
```



### Booking - CreateBooking


```cURL
 curl -X POST \
  https://restful-booker.herokuapp.com/booking \
  -H 'Content-Type: application/json' \
  -d '{
    "firstname" : "Jim",
    "lastname" : "Brown",
    "totalprice" : 111,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2018-01-01",
        "checkout" : "2019-01-01"
    },
    "additionalneeds" : "Breakfast"
}'
```

### Booking - UpdateBooking



```cURL
curl -X PUT \
  https://restful-booker.herokuapp.com/booking/315 \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Cookie: token=abc123' \
  -d '{
    "firstname" : "James",
    "lastname" : "Brown",
    "totalprice" : 111,
    "depositpaid" : true,
    "bookingdates" : {
        "checkin" : "2018-01-01",
        "checkout" : "2019-01-01"
    },
    "additionalneeds" : "Breakfast"
}'
```

### Booking - PartialUpdateBooking



```cURL
 curl -X PATCH \
  https://restful-booker.herokuapp.com/booking/1 \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Cookie: token=abc123' \
  -d '{
    "firstname" : "James",
    "lastname" : "Brown"
}'
```

### Booking - DeleteBooking


```cURL
 curl -X DELETE \
  https://restful-booker.herokuapp.com/booking/1 \
  -H 'Content-Type: application/json' \
  -H 'Cookie: token=abc123'
```

