# nvidia_smi

The following dashboards are provided for use with data from the Telegraf [nvidia_smi](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nvidia-smi) input.

## NVIDIA: GPU Performance

![NVIDIA: GPU Performance](https://user-images.githubusercontent.com/10326954/58805102-ab6c1a80-8613-11e9-86e3-a74979a8573f.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.nvidia_smi]]
  # Optional: path to nvidia-smi binary, defaults to $PATH via exec.LookPath
  #bin_path = "/usr/bin/nvidia-smi"

  # Optional: timeout for GPU polling
  #timeout = "5s"
```
