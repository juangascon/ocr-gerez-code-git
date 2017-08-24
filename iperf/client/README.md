This Dockerfile launches an iperf client sending 100Kbps traffic to a server at ip '172.17.0.2' who is listening to port: 9435 and prints reports at intervals of 1 second

These values can be changed via the environnement values:

* IPERF_SRV_IP 172.17.0.2
* IPERF_SRV_PORT 9435
* IPERF_INTERVAL 1
* IPERF_BW 100K

The docker is built as follows:

~$ sudo docker build -t vnf-iperf_client .

The docker should be called as follows:

~$ sudo docker run -ti --rm -P [-e "IPERF_SRV_PORT=9435"] --name vnf-iperf_client vnf-iperf_client:latest
