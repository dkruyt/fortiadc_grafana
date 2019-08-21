FortiADC is is a application delivery controllers (loadbalancer). The devices metrics are availalbe via SNMP. So it's quite easy to collect those and display them in Grafana.

![connectionpool-1](https://blog.kruyt.org/content/images/2018/07/connectionpool-1.png)

### Pre Install

Make sure you have installed [InfluxDB](https://portal.influxdata.com/downloads) as the time-series database [Telegraf](https://portal.influxdata.com/downloads) as collector first.
Optional you can also include the FortiADC logs when they are in elasticsearch. I use the Greylog sollution for this.

### Quick Start

Get the latest files, at [my GitHub page](https://github.com/dkruyt/fortiadc_grafana)

* Enable SNMP on your FortiADC
* Put fortiadc.conf in your `/etc/telegraf/telegraf.d` directory
* Edit the community string as appropriate
* Edit the SNMP verion as appropriate
* Edit the 'agents' list to include all of your monitored FortiADC loadbalancers
* Put the files in the mibs dir `/usr/share/snmp/mibs`
* Import the Grafana dashboard

### Screenshot

After you setup all, you should have a dashboard like this.

![screencapture-fortiadc-blur](https://blog.kruyt.org/content/images/2018/07/screencapture-fortiadc-blur.png)



