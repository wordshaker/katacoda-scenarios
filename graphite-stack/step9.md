## Duration / Latency 

We have yet to measure the duration from when each request is made, to when a response is returned. 

First, to measure the duration of the successful response in the query select `stats` `timers` `response-api` `code` `200` `count`.  In the Functions for the same query select `transformNull()` `averageSeries()` `alias(success response time)`

The erroring responses are very similar. For this query select `stats` `timers` `response-api` `code` `500` `count`.  In the Functions for the same query select `transformNull()` `averageSeries()` `alias(error response time)`

Go to the _display_ tab and select series overrides. The first override will be for the successful response. Use the alias _success response time_ followed by `Lines: true` `Line fill:2` `Y-axis:2`

This moves the response times to a second y-axis on the right hand side.

We will do the same for erroring response time. Add a second override using the alias _error response time_ followed by `Lines: true` `Line fill:2` `Y-axis:2`.