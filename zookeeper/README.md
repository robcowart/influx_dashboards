# zookeeper

The following dashboards are provided for use with data from the Telegraf [zookeeper](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#zookeeper) input.

## Zookeeper: Performance

![screenshot 2019-01-08 at 20 15 05](https://user-images.githubusercontent.com/10326954/50853677-31e14080-1383-11e9-8487-0236f9f52de6.png)

## Zookeeper: Resources

![screenshot 2019-01-08 at 20 14 37](https://user-images.githubusercontent.com/10326954/50853676-31e14080-1383-11e9-9717-e2944012cab1.png)

## Zookeeper: Namespace

![screenshot 2019-01-08 at 20 16 20](https://user-images.githubusercontent.com/10326954/50853679-31e14080-1383-11e9-953d-68139ee1aa98.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.zookeeper]]
  servers = ["192.0.2.11:2181"]

  timeout = "5s"

  # Optional TLS Config
  #tls_ca = "/etc/telegraf/ca.pem"
  #tls_cert = "/etc/telegraf/cert.pem"
  #tls_key = "/etc/telegraf/key.pem"

  # Use TLS but skip chain & host verification
  #insecure_skip_verify = true
```
