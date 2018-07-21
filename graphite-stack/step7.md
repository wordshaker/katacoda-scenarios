
Go back to the Grafana tab. 

On the left hand click hover on the `+` symbol and select the option to create a dashboard.

The first panel we will add with be a graph. Select the appropriate icon, click on the panel title and select edit.

Select `graphite as your Data Source`.

For the first query select `stats` `timers` `response-api` `code` `200` `count`. Ensure that the time scale set at the top is set to the past hour. You should see a count for the amount of times you clicked the Success Code command in the previous step.

For the first query select `stats` `timers` `response-api` `code` `500` `count`. You should see a count for the amount of times you clicked the  command to return Internal Server Errors in the previous step.

Congratulations! You have made your first graph using the stack!