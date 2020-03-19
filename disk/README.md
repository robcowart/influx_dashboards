# disk

The following dashboards are provided for use with data from the Telegraf [disk](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#disk) input.

## Disk: Capacity

![Disk: File System Capacity](https://user-images.githubusercontent.com/10326954/77057026-9c542e80-69d3-11ea-8166-774fb7c18a2d.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.disk]]
  # By default stats will be gathered for all mount points. Set mount_points will restrict the stats to only the
  # specified mount points.
  #mount_points = ["/"]

  # Ignore mount points by filesystem type.
  ignore_fs = ["tmpfs", "devtmpfs", "devfs", "overlay", "aufs", "squashfs", "shm", "/dev/loop*"]

  [inputs.disk.tagdrop]
    path = [ "/run/docker/runtime-runc/moby/*" ]
```
