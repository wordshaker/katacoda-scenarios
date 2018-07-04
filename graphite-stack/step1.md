
A [network](https://docs.docker.com/engine/reference/commandline/network_create/#connect-containers) enables docker containers, services and workloads to connect together. We set up the network for StatsD, Graphite and Grafana to talk to each other. 

For the purpose of this exercise we will be using the default from of network - a bridge. This is typical for applications that are running in standalone containers that need to communicate with each other. 

## Task

For the purpose of this task enter the following command into the terminal

`docker network create monitoring`{{execute}}
