# RED and The Four Golden Signals

So far, we have set up StatsD, Graphite and Grafana and ran an API that returns given responses. Now we have come to the point where we need to build our dashboard. 

As we have set up an API that you can manipulate the response of, we can demonstrate some useful ways we can monitor the behaviour of API's and why.

RED, which is discussed in [this blog written by Peter Bourgon],(https://peter.bourgon.org/blog/2016/02/07/logging-v-instrumentation.html) is a mnemonic coined by Tom Wilkie. Much like [Brendan's Gregg USE methods for measuring system resources and services](http://www.brendangregg.com/usemethod.html), RED is suggested as baseline measurements for API's.

- **R**ate - a count of requests over time

- **E**rror - a count of error over time

- **D**uration - the time between request and response.

These principles are echoed in the [Google Four Golden Signals mentioned in the Monitoring Distributed Systems chapter of their SRE book](https://landing.google.com/sre/book/chapters/monitoring-distributed-systems.html). 

1. Latency - the time between request and response but with a focus of the difference between successful and erroring requests.

2. Traffic - requests per second. A measure of the load on the API.

3. Errors - same as before, a count of errors.

4. Saturation - what percentage of your systems resources is currently in use.

In this next section, we shall build a dashboard reflecting the above principles focusing on the principles that overlap between these two frameworks. Saturation is difficult to demonstrate accurately with the set up and timeframe for this demo. Ideally you would need to have conducted load testing to find out the capacity of your systems, and set alerts or visual cues around when your are getting close enough to that capacity that you would need to take action. 