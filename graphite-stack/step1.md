This is your first step.

## Task

<<<<<<< HEAD
Create Network:

`docker network create monitoring`{{execute}}
=======
Run graphite:

`docker run -d --name graphite -p 80:80 -p 2003-2004:2003-2004 -p 2023-2024:2023-2024 -p 8125:8125/udp -p 8126:8126 --network monitoring graphiteapp/graphite-statsd`{{execute}}
>>>>>>> b2f7637719e6d51f27ca4acfc21d733e1dcb3db7
