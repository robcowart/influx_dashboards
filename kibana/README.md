# kibana

The following dashboards are provided for use with data from the Telegraf [kibana](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#kibana) input.

## Kibana: Performance

![Kibana: Performance](https://user-images.githubusercontent.com/10326954/58793481-80bf9900-85f6-11e9-9eb9-5f20ac2d0325.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.kibana]]
  servers = ["http://192.2.0.1:5601"]
  timeout = "5s"

  username = "elastic"
  password = "changeme"

  # tls_ca = "/etc/telegraf/ca.pem"
  # tls_cert = "/etc/telegraf/cert.pem"
  # tls_key = "/etc/telegraf/key.pem"
  # insecure_skip_verify = false

```
