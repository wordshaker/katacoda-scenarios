# RED and The Four Golden Signals

So far, we have set up StatsD, Graphite and Grafana, ran an API that returns given responses and now we have come to the point where we need to build our dashboard. 

As we have set up an API that is you can manipulate the response of, we can demonstrate some useful ways we can monitor the behaviour of API's and why.

RED is discussed in [this blog written by Peter Bourgon](https://peter.bourgon.org/blog/2016/02/07/logging-v-instrumentation.html) is a mnemonic coined by Tom Wilkie. Much like [Brendan's Gregg USE methods for measuring system resources](http://www.brendangregg.com/usemethod.html), RED is suggested as baseline measurements for API's.

- **R**ate - a count of requests over time

- **E**rror - a count of error over time

- **D**uration - the time between request and response.

These principles are echoed in the [Google Four Golden Signals mentioned in the Distributed Systems chapter of their SRE book](https://landing.google.com/sre/book/chapters/monitoring-distributed-systems.html). 

1. Latency - the time between request and response but with a focus of the difference between successful and erroring requests.

2. Traffic - requests per second. A measure of the load on the API.

3. Errors - same as before, a count of errors.

4. Saturation - measures of the systems utilisation. Is the memory, I/O or CPU reaching capacity for example.

In this next section, we shall build a dashboard reflecting the above principles focusing on the principles that overlap between these two frameworks. Saturation is difficult to set up for the current set up and within the timeframe of this demo.