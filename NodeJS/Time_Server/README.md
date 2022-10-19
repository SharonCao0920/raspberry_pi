# Project

Time Server + Parsing Time Project on Raspberry Pi

**[Time Server Project Google Slides](https://docs.google.com/presentation/d/1XAkSt4FUhRcIo1oGNAgIyJs7iM4hXi_XtbE2ea6yzG4/edit?usp=sharing)**

## Introduction

**Write a TCP time server!**
Your server should listen to TCP connections on the port provided by the first argument to your program. For each connection you must write the 
current date & 24 hour time in the format of "YYYY-MM-DD hh:mm"

**Write an HTTP server**
that serves JSON data when it receives a GET request to the path '/api/parsetime'. Expect the request to contain a query string with a key 'iso' and 
an ISO-format time as the value.


## Design

### TCP time server

**Step 1:** on the server side
* $ node time_server.js 8000

**Step 2:** On the client side browser
* http://localhost:8000/


### HTTP server

**Step 1:** On the server
$ node http_json_api_server.js 8000

**Step 2:** on the client browser
http://localhost:8000/api/parsetime?iso=2013-08-10T12:10:15.474Z

**Step 3:** on the client browser
http://localhost:8000/api/unixtime?iso=2013-08-10T12:10:15.474Z


## Implementation

* Code

   * http_json_api_server.js
   * time_server.js
      * MapReduce Program

## Test

Process to test the project.


## Enhancement

Change the program to use current time in previous formats.



## Conclusion
TCP Server, HTTP Server runs no problem on Raspberry Pi with node.js. 



