# nvidia_smi

The following dashboards are provided for use with data from the Telegraf [nvidia_smi](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#nvidia-smi) input.

## NVIDIA: GPU Performance

![NVIDIA: GPU Performance](https://user-images.githubusercontent.com/10326954/68026205-45adb880-fcaf-11e9-944a-c7e34c4d988b.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.nvidia_smi]]
  # Optional: path to nvidia-smi binary, defaults to $PATH via exec.LookPath
  #bin_path = "/usr/bin/nvidia-smi"

  # Optional: timeout for GPU polling
  #timeout = "5s"
```
