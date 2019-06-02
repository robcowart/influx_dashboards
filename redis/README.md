# redis

The following dashboards are provided for use with data from the Telegraf [redis](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nginx) input. This input will produce both the `redis` and `redis_keyspace` measurements.

## Redis: Server Resources

![Redis: Server Resources](https://user-images.githubusercontent.com/10326954/50771309-894fb580-128a-11e9-8760-efe2f0820a3b.png)

## Redis: Keystore

![Redis: Keystore](https://user-images.githubusercontent.com/10326954/50771319-953b7780-128a-11e9-91c5-e772b389c419.png)

## Redis: Client Connections

![Redis: Client Connections](https://user-images.githubusercontent.com/10326954/50771316-8fde2d00-128a-11e9-8f26-ebbc2a7d6321.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.redis]]
  servers = ["tcp://192.2.0.1:6379"]
  password = "changeme"

  # Optional TLS Config
  #tls_ca = "/etc/telegraf/ca.pem"
  #tls_cert = "/etc/telegraf/cert.pem"
  #tls_key = "/etc/telegraf/key.pem"

  # Use TLS but skip chain & host verification
  #insecure_skip_verify = true
```
