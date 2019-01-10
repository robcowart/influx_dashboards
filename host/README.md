# host

The following dashboards are provided for use with data from the following Telegraf input plugins:

* [cpu](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#cpu)
* [mem](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#mem)
* [processes](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#processes)
* [swap](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#swap)
* [system](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#system)

## Host: Compute Performance

![Host: Compute Performance](https://user-images.githubusercontent.com/10326954/50965684-f9507c80-14d2-11e9-983c-2e7cc920a584.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```
[[inputs.cpu]]
  # Whether to report per-cpu stats or not
  percpu = true
  # Whether to report total system cpu stats or not
  totalcpu = true
  # If true, collect raw CPU time metrics.
  collect_cpu_time = false
  # If true, compute and report the sum of all non-idle CPU states.
  report_active = false

[[inputs.mem]]

[[inputs.processes]]

[[inputs.swap]]

[[inputs.system]]
```
