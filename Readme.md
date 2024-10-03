# Restful-booker Apis curls 
In this repository you will find the curls of APIs
authorization, Getbooking, getbookingbyID, UpdateBooking, PartialUpdateBooking, deleteBooking and Ping


///Authorization

curl -X POST \
  https://restful-booker.herokuapp.com/auth \
  -H 'Content-Type: application/json' \
  -d '{
    "username" : "admin",
    "password" : "password123"
}'


//Get bookingID

curl -i https://restful-booker.herokuapp.com/booking


//Get bookingbyID

curl -i https://restful-booker.herokuapp.com/booking/1

//Update Booking

curl -X PUT \
  https://restful-booker.herokuapp.com/booking/1 \
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

//Partial update booking

curl -X PATCH \
  https://restful-booker.herokuapp.com/booking/1 \
  -H 'Content-Type: application/json' \
  -H 'Accept: application/json' \
  -H 'Cookie: token=abc123' \
  -d '{
    "firstname" : "James",
    "lastname" : "Brown"
}'

//Delete booking


///Delete booking 
curl -X DELETE \
  https://restful-booker.herokuapp.com/booking/1 \
  -H 'Content-Type: application/json' \
  -H 'Cookie: token=abc123'

//Ping

curl -i https://restful-booker.herokuapp.com/ping