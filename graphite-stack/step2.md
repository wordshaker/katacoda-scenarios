This is your first step.

## Task

Run graphite, carbon and statsD:

`docker run -d --name graphite -p 80:80 -p 2003-2004:2003-2004 -p 2023-2024:2023-2024 -p 8125:8125/udp -p 8126:8126 --network monitoring graphiteapp/graphite-statsd`{{execute}}
