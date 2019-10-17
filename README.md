# Influx Dashboards

This project provides Chronograf dashboards for use with data produced by various Telegraf input plugins, and stored in InfluxDB.

![Influx Dashboards](https://user-images.githubusercontent.com/10326954/58766393-516d4580-857e-11e9-8be4-7dbbff55917d.png) 

The following dashboard collections are provided:

Dashboards | Telegraf Inputs
--- | ---
[disk](https://github.com/robcowart/influx_dashboards/tree/master/disk) | [disk](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#disk)
[diskio](https://github.com/robcowart/influx_dashboards/tree/master/diskio) | [diskio](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#diskio)
[docker](https://github.com/robcowart/influx_dashboards/tree/master/docker) | [docker](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#docker), [docker_log](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#docker_log)
[host](https://github.com/robcowart/influx_dashboards/tree/master/host) | [cpu](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#cpu), [kernel](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#kernel), [mem](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#mem), [processes](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#processes), [swap](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#swap), [system](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#system)
[influxdb](https://github.com/robcowart/influx_dashboards/tree/master/influxdb) | [influxdb](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#influxdb)
[kibana](https://github.com/robcowart/influx_dashboards/tree/master/kibana) | [kibana](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#kibana)
[kubernetes](https://github.com/robcowart/influx_dashboards/tree/master/kubernetes) | [kubernetes](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#kubernetes), [system](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#system)
[net](https://github.com/robcowart/influx_dashboards/tree/master/net) | [net](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#net)
[nginx](https://github.com/robcowart/influx_dashboards/tree/master/nginx) | [nginx](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nginx)
[nvidia_smi](https://github.com/robcowart/influx_dashboards/tree/master/nvidia_smi) | [nvidia_smi](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nvidia-smi)
[redis](https://github.com/robcowart/influx_dashboards/tree/master/redis) | [redis](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#redis)
[sensors](https://github.com/robcowart/influx_dashboards/tree/master/sensors) | [sensors](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#sensors)
[smart](https://github.com/robcowart/influx_dashboards/tree/master/smart) | [smart](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#smart)
[zookeeper](https://github.com/robcowart/influx_dashboards/tree/master/zookeeper) | [zookeeper](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#zookeeper)

## Importing Dashboards

The dashboards themselves are easily imported from the Chronograf user interface. An example telegraf input configuration is also provided in the README.md for each dashboard collection.

Please refer to the Chronograf documentation for instructions to [import dashboards](https://docs.influxdata.com/chronograf/latest/administration/import-export-dashboards/#importing-a-dashboard).

## Examples

### Host: Compute Performance

![Host: Compute Performance](https://user-images.githubusercontent.com/10326954/50965684-f9507c80-14d2-11e9-983c-2e7cc920a584.png)

### Sensors: System Environment Health

![Sensors: System Environment Health](https://user-images.githubusercontent.com/10326954/50735499-6a7cf080-11b0-11e9-95f4-a0aa11ace4a2.png)

### Net: Interface Performance

![Net: Interface Performance](https://user-images.githubusercontent.com/10326954/50738526-467fd600-11d5-11e9-89ef-fcd15ec0e6a2.png)

### NGiNX: Connections

![NGiNX: Connections](https://user-images.githubusercontent.com/10326954/50740156-b8aee580-11ea-11e9-8d41-c733bec82b85.png)
