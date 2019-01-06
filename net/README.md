# net

The following dashboards are provided for use with data from the Telegraf [net](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#net) input.

## Net: Interface Performance

The Interface Performance dashboard allows users to investigate network traffic volume, as well as identify issues related to dropped or errored packets.

Template variables are provided to allow easy selection from the network interface to be viewed.

![Net: Interface Performance](https://user-images.githubusercontent.com/10326954/50738526-467fd600-11d5-11e9-89ef-fcd15ec0e6a2.png)

## Net: Interface Metric Explorer

The Interface Metric Explorer dashboard allows users to explore the various metrics which may be collected for a network interface. The dashboard allows for two sets of _host_, _interface_ and _metrics_ to be selected, which allows for easy data comparisons.

As the network interface metrics are counters, all queries leverage the [non_negative_derivative()](https://docs.influxdata.com/influxdb/v1.7/query_language/functions/#non-negative-derivative) function and express values as _per second_.

![Net: Interface Metric Explorer](https://user-images.githubusercontent.com/10326954/50738541-657e6800-11d5-11e9-875e-6398318d9d45.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```
[[inputs.net]]
  # By default, telegraf gathers stats from any up interface (excluding loopback). Setting interfaces will tell it to
  # gather these explicit interfaces, regardless of status.
  #interfaces = ["eth0"]
  
  # On linux systems telegraf also collects protocol stats. Setting ignore_protocol_stats to true will skip reporting
  # of protocol metrics.
  #ignore_protocol_stats = false
```
