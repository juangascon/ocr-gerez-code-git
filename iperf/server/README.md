This Dockerfile launches an iperf server listening to port 9435 and reports at intervals of 1 second

These values can be changed via the environnement values:

* IPERF_SRV_PORT 9435
* IPERF_INTERVAL 1

The docker is built as follows:

~$ sudo docker build -t vnf-iperf_srv .

The docker should be called as follows:

~ $ sudo docker run -ti --rm -P [-e "IPERF_SRV_PORT=9435"] --name vnf-iperf_srv vnf-iperf_srv:latest
