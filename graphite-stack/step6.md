In order to have some statistics displaying in Grafana, we need to use the API.

Below are two cURL commands that POST to our response API. 

`curl -i -d {"expectedReturnedCode":"200"}` signifies the request includes the data/body of `{"expectedReturnedCode":"200"}`. A header is passed as part of this request showing that the content type of the body is JSON `-H "Content-Type: application/json"`. The final part of the states the HTTP verb used `-X POST` and the endpoint the request is being sent to `http://docker:5000/api/code`.  

You can run the following commands as many times as you wish.

Success codes:

`curl -i -d '{"expectedReturnedCode":"200"}' -H "Content-Type: application/json" -X POST http://docker:5000/api/code`{{execute}}

Internal Server Errors:

`curl -i -d '{"expectedReturnedCode":"500"}' -H "Content-Type: application/json" -X POST http://docker:5000/api/code`{{execute}}