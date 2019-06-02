# disk

The following dashboards are provided for use with data from the Telegraf [disk](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#disk) input.

## Disk: File System Capacity

![Disk: File System Capacity](https://user-images.githubusercontent.com/10326954/50955040-699dd480-14b8-11e9-8676-0a685822f696.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.disk]]
  # By default stats will be gathered for all mount points. Set mount_points will restrict the stats to only the
  # specified mount points.
  #mount_points = ["/"]

  # Ignore mount points by filesystem type.
  ignore_fs = ["tmpfs", "devtmpfs", "devfs", "overlay", "aufs", "squashfs", "shm", "/dev/loop*"]
```
