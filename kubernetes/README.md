# kubernetes

The following dashboards are provided for use with data from the Telegraf [kubernetes](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#kubernetes) input.

## Kubernetes: Node Resources

![Kubernetes: Node Resources](https://user-images.githubusercontent.com/10326954/62412381-c520e280-b601-11e9-86a2-8f7e24bdf3b0.png)

## Kubernetes: System Containers

![Kubernetes: System Containers](https://user-images.githubusercontent.com/10326954/62412389-cfdb7780-b601-11e9-9540-fddce3835d68.png)

## Kubernetes: Pod Containers

![Kubernetes: Pod Containers](https://user-images.githubusercontent.com/10326954/62412391-d538c200-b601-11e9-9db5-13b224436009.png)

## Kubernetes: Pod Networks

![Kubernetes: Pod Networks](https://user-images.githubusercontent.com/10326954/62412393-d79b1c00-b601-11e9-9c91-10d8e2346cb2.png)

## Kubernetes: Pod Volumes

![Kubernetes: Pod Volumes](https://user-images.githubusercontent.com/10326954/62412394-d964df80-b601-11e9-82fb-86538dc96c76.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.system]]
# The system input is needed to get the number of CPU cores.

[[inputs.kubernetes]]
  # URL for the kubelet
  url = "https://192.2.0.1:10250"

  # Use bearer token for authorization
  #bearer_token = /path/to/bearer/token

  # Set response_timeout (default 5 seconds)
  #response_timeout = "5s"

  # Optional TLS Config
  #tls_ca = /path/to/cafile
  tls_cert = '/etc/kubernetes/pki/kubelet-client.crt'
  tls_key = '/etc/kubernetes/pki/kubelet-client.key'
  insecure_skip_verify = true
```

> NOTE: The read-only port 10255 is deprecated in more recent versions of Kubernetes. You will need to use the secure port, 10250. This requires that you configure Kubernetes security to allow for the use of either a bearer token or certificates for access.
