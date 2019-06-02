# smart

The following dashboards are provided for use with data from the Telegraf [smart](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#smart) input.

## S.M.A.R.T.

![S.M.A.R.T.](https://user-images.githubusercontent.com/10326954/50967373-44b95980-14d8-11e9-8449-f3c9faa9b7d0.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```toml
[[inputs.smart]]
  # Optionally specify the path to the smartctl executable.
  #path = "/usr/bin/smartctl"

  # On most platforms smartctl requires root access. Setting 'use_sudo' to true will make use of sudo to run smartctl.
  # Sudo must be configured to to allow the telegraf user to run smartctl with out password.
  #use_sudo = false

  # Skip checking disks in this power mode. Defaults to "standby" to not wake up disks that have stoped rotating. See
  # --nocheck in the man pages for smartctl. smartctl version 5.41 and 5.42 have faulty detection of power mode and
  # might require changing this value to "never" depending on your disks.
  #nocheck = "standby"

  # Gather detailed metrics for each SMART Attribute. Defaults to "false".
  #attributes = false

  # Optionally specify devices to exclude from reporting.
  #excludes = [ "/dev/pass6" ]

  # Optionally specify devices and device type. If unset, a scan (smartctl --scan) for S.M.A.R.T. devices will done and
  # all found will be included except for the excluded in excludes.
  #devices = [ "/dev/ada0 -d atacam" ]
```
