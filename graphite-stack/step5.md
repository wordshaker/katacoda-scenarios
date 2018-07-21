
## Run the api

The monitoring stack is up and running. What we need is some metrics and stats to display.

For the purpose of this exercise I have created a very simple API that you can send an integer to, and it will respond with the corresponding HTTP Status Code.

To run the API, input the following command into the terminal.

`docker run -d --name response-api -t -p 5000:5000 --network monitoring wordshaker90/response-api:latest`{{execute}}
