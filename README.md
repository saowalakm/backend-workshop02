# Springboot Command Run

1. Basic command
* gradlew
* gradlew test      //test
* gradlew bootRun   //run for environment
* gradlew bootJar   //run for deploy 

2. Fix errors
* gradlew clean
* set java_home=<location java>jdk folder>
* gradlew test 
* wait ...
or
* build.gradle
* edit line 9 sourceCompatibility ='8'

3. Set java path
* echo %java_home%
* set path=.;%java_home%\bin;%path%

---------------------------------------------------------

Example for demo

* Step_01
http://localhost:8080/users
GET /users
Response code = 200
[
    {
        "id": 1,
        "name": "User 1"
    },
    {
        "id": 2,
        "name": "User 2"
    }
}

http://localhost:8080/users/1
Get user information with id + GET /user/<id>
{
    "id": 1,
    "name": "User 1"
}

* Step_02
http://localhost:8080/users/?page=1
{
  "usersResponseList": [
    {
      "id": 1,
      "name": "User 1"
    },
    {
      "id": 2,
      "name": "User 2"
    },
    {
      "id": 3,
      "name": "User 3"
    }
  ],
  "page": 1,
  "itemPerPage": 10
}

* Postman
Create a new user
+ POST /users
{
    "name": "somkiat",
    "age": 30
}
Response
{
    "id": 1234,
    "name": "somkiat",
    "age": 30
}