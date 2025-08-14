# Netdata Docker Task

## Task Objective
Run **Netdata** inside a Docker container and access the monitoring dashboard on `http://localhost:19999`.

## Steps Followed
1. Pulled the latest Netdata image:
   ```bash
   docker run -d --name=netdata \
     -p 19999:19999 \
     -v netdataconfig:/etc/netdata \
     -v netdatalib:/var/lib/netdata \
     -v netdatacache:/var/cache/netdata \
     --restart unless-stopped \
     netdata/netdata

