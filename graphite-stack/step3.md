## Let's get visualising

## Run Grafana

Now we have the ability to record our metrics, we need to be able to display them in a useful format. This is where Grafana comes in. Grafana is a dashboarding / visualisation UI that can be provided with a variety of data sources.

To get Grafana running, input the following command into the terminal

`docker run -d --name grafana -p 3000:3000 --network monitoring grafana/grafana`{{execute}}

Again we are instructing Docker that Grafana is going to be on the monitoring network so that it can get information from Graphite. We also provide which port it will be running on.

You can see Grafana is to be run on port 3000. Click onto the tab at the top of the terminal titled `Display 3000`. This will open a new tab. 

Instructions on what to do next are shown in the next step.