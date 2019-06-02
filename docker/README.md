# docker

The following dashboards are provided for use with data from the Telegraf [docker](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#docker) input.

## Docker: Engine

![Docker: Engine](https://user-images.githubusercontent.com/10326954/58759127-68cc1480-8525-11e9-8474-de1b08844afe.png)

## Docker: Container Compute Performance

![Docker: Container Compute Performance](https://user-images.githubusercontent.com/10326954/58761899-6976a200-8549-11e9-9247-5302a0efe099.png)

## Docker: Device Block I/O

![Docker: Device Block I/O](https://user-images.githubusercontent.com/10326954/58760563-d8e49580-8539-11e9-9818-3e036496bc9d.png)

## Docker: Container Block I/O

![Docker: Container Block I/O](https://user-images.githubusercontent.com/10326954/58760537-74c1d180-8539-11e9-85c1-eb46323b7710.png)

## Docker: Container Network Performance

![Docker: Container Network Performance](https://user-images.githubusercontent.com/10326954/58762503-d6416a80-8550-11e9-857e-3c99560526d1.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.docker]]
  # Docker Endpoint. To use TCP, set endpoint = "tcp://[ip]:[port]". To use environment variables (ie, docker-machine), set endpoint = "ENV"
  endpoint = "unix:///var/run/docker.sock"

  # Set to true to collect Swarm metrics(desired_replicas, running_replicas)
  gather_services = false

  # Only collect metrics for these containers, collect all if empty
  container_names = []

  # Containers to include and exclude. Globs accepted. Note that an empty array for both will include all containers
  container_name_include = []
  container_name_exclude = []

  # Container states to include and exclude. Globs accepted. When empty only containers in the "running" state will be captured.
  #container_state_include = []
  #container_state_exclude = []

  # Timeout for docker list, info, and stats commands
  timeout = "5s"

  # Whether to report for each container per-device blkio (8:0, 8:1...) and network (eth0, eth1, ...) stats or not
  perdevice = true
  # Whether to report for each container total blkio and network stats or not
  total = false
  # Which environment variables should we use as a tag
  #tag_env = ["JAVA_HOME", "HEAP_SIZE"]

  # docker labels to include and exclude as tags. Globs accepted. Note that an empty array for both will include all labels as tags
  docker_label_include = []
  docker_label_exclude = []

  # Optional TLS Config
  #tls_ca = "/etc/telegraf/ca.pem"
  #tls_cert = "/etc/telegraf/cert.pem"
  #tls_key = "/etc/telegraf/key.pem"
  #insecure_skip_verify = false
```
