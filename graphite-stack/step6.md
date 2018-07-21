In order to have some statistics displaying in Grafana, we need to use the API.

## Hit the API

Success codes:

`curl -i -d '{"expectedReturnedCode":"200"}' -H "Content-Type: application/json" -X POST http://docker:5000/api/code`{{execute}}

Internal Server Errors:

`curl -i -d '{"expectedReturnedCode":"500"}' -H "Content-Type: application/json" -X POST http://docker:5000/api/code`{{execute}}