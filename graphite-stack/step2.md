Now we have our network setup, lets get our stack set up. 

## Our monitoring stack

We will be using StatsD for telemetry, and Graphite as our data source behind Grafana, our choice of visualisation tool.

[StatsD](https://github.com/etsy/statsd) was created by Etsy. It's a background process that listens for messages on a UDP port, which it then parses / aggregates and, in this case, passes on to Graphite. StatsD is well supported, lightweight & not overly complex.

[Graphite](http://graphiteapp.org/) is the next layer of the stack. Graphite is composed of Carbon, Whisper and Graphite-Web. Carbon listens for the time-series data (from StatsD), Whisper stores the data and Graphite-Web is the API for rendering graphs and visualisations, and has its own UI for creating them.

##  Run Graphite, Carbon and StatsD

The images for Graphite and StatsD should have been pulled down in the background when you started this course using `docker pull graphiteapp/graphite-statsd`.

## Task 

To run them, enter the following command into the terminal

`docker run -d --name graphite -p 80:80 -p 2003-2004:2003-2004 -p 2023-2024:2023-2024 -p 8125:8125/udp -p 8126:8126 --network monitoring graphiteapp/graphite-statsd`{{execute}}

This is instructing docker to run the image, which ports it should be running on, which network its needs to be on and that it's a UDP connection.
