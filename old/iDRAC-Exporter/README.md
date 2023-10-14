# iDRAC Exporter

This application is meant to be deployed to Kubernetes using Kustomize.

* **Website**: https://www.influxdata.com/time-series-platform/telegraf/
* **Container Image:** https://hub.docker.com/_/telegraf

<hr>

## Notes

* You will need a InfluxDB database to use the iDRAC Exporter. 
* You will need an iDRAC compatible server to use the iDRAC Exporter.

<hr>

## Instructions

An example overlay is provided from my environment. Simply create a new overlay using it as an example and deploy it to your environment like so:

   ```bash
    kustomize build iDrac-Exporter/overlays/example | kubectl apply -f-
   ```

Don't forget to update `telegraf.conf` according to your environment. Options are documented [here](https://github.com/influxdata/telegraf/blob/master/docs/CONFIGURATION.md).
