# influxdb

The following dashboards are provided for use with data from the Telegraf [influxdb](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#influxdb) input.

## InfluxDB: Databases

![InfluxDB: Databases](https://user-images.githubusercontent.com/10326954/58766265-b4f67380-857c-11e9-86e2-ee6194df24bb.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.influxdb]]
  urls = [
    "http://192.0.2.1:8086/debug/vars"
  ]

  # tls_ca = "/etc/telegraf/ca.pem"
  # tls_cert = "/etc/telegraf/cert.pem"
  # tls_key = "/etc/telegraf/key.pem"
  # insecure_skip_verify = false

  ## http request & header timeout
  timeout = "5s"
```
