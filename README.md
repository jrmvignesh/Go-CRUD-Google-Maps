# cmpe273-googlemapslocation
This program is about setting up a REST service using golang with the help of httprouter, focused on CRUD services to a mongodb backend.

Before executing the program we need HTTPROUTER package.We first need to fetch the package with go get.
$ go get github.com/julienschmidt/httprouter

mgo is used as mongo driver from golang. We will be using the following packages.
$ go get gopkg.in/mgo.v2
$ go get gopkg.in/mgo.v2/bson


How to execute : 
1) Open git terminal. Run the file 

go run main.go

2) While the connection is open, open another terminal and run the CURL commands for POST,GET,PUT AND DELETE.

Some example of CURL commands for the program
POST command :

curl  -H "Content-Type: application/json" -X POST -d '{"Name" : "John Smith", "Address" : "1600 Amphitheatre Parkway", "City" : "Mountain View" , "State": "CA", "Zip" : "94043"}' http://127.0.0.1:8080/locations

DELETE command :

curl -X DELETE http://127.0.0.1:8080/locations/56292aef791dee14bccec968

GET command :

curl -X GET http://127.0.0.1:8080/locations/56292aef791dee14bccec968


PUT command :

curl -H "Content-Type: application/json" -X PUT -d '{"Name" : "Vignesh","Address" : "101 E San Fernando" , "City" : "San Jose",   "State" : "CA",   "Zip" : "95192"}' http://127.0.0.1:8080/locations/56292aef791dee14bccec968
