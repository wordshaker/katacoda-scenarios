##  Rate / Traffic & Error's

Go back to the Grafana tab. 

On the left hand click hover on the `+` symbol and select the option to create a dashboard.

The first panel we will add with be a graph. Select the appropriate icon, click on the panel title and select edit.

Select `graphite as your Data Source`.

First lets display the rate and latency of successful calls. We will put the response times and count of successful calls in the same graph.

The first query would be `stats` `timers` `response-api` `code` `2*` `count`.  In the functions for the same query select `transformNull()` `sumSeries()` `alias(2XX requests count)`

Ensure that the time scale set at the top is set to the past hour. You should see a count for the amount of times you clicked the Success Code command in the previous step.

Now add the erroring calls.

For the second query select `stats` `timers` `response-api` `code` `5*` `count`.  In the functions for the same query select `transformNull()` `sumSeries()` `alias(5XX requests count)`

You should see a count for the amount of times you clicked the  command to return Internal Server Errors in the previous step.

Congratulations! You have made your first graph using the stack!