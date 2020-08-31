# nginx

The following dashboards are provided for use with data from the Telegraf [nginx](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nginx) input.

## NGiNX: Connections

The Connections dashboard allows users to investigate an NGiNX server's connection volume.

Template variables are provided to allow easy selection of the NGiNX server to be viewed.

![NGiNX: Connections](https://user-images.githubusercontent.com/10326954/50740156-b8aee580-11ea-11e9-8d41-c733bec82b85.png)

## NGiNX Server Configuration

The NGiNX server must be configured to load the `stub_status` module. The following example will make the statistics available at `/nginx_status`.

```text
location /nginx_status {
  stub_status;
  allow 127.0.0.1;
  allow 192.168.0.0/16;
  allow 10.0.0.0/16;
  deny all;
}
```

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.nginx]]
  # An array of Nginx stub_status URI to gather stats.
  urls = ["http://192.0.2.11/nginx_status"]

  # Optional TLS Config
  #tls_ca = "/etc/telegraf/ca.pem"
  #tls_cert = "/etc/telegraf/cert.cer"
  #tls_key = "/etc/telegraf/key.key"
  
  # Use TLS but skip chain & host verification
  insecure_skip_verify = true

  # HTTP response timeout (default: 5s)
  response_timeout = "5s"
```
