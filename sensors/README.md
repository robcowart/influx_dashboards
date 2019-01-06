# sensors

The following dashboards are provided for use with data from the Telegraf [sensors](https://docs.influxdata.com/telegraf/latest/plugins/inputs/#sensors) input.

## Sensors: System Environment Health

The System Environment Health dashboards allows users to easily investigate data produced by `lm-sensors` which has been collected by the Telegraf `sensors` input.

The dashboard is organized around three columns:

* The first column provides the current, or `last`, value of the selected sensors.
* The second column provides a historical graph of the selected sensors over the time range specified.
* The third column combines all instances of the row's sensor type.

Template variables are provided to allow easy navigation from one sensor value to another.

![Sensors: System Environment Health](https://user-images.githubusercontent.com/10326954/50735499-6a7cf080-11b0-11e9-95f4-a0aa11ace4a2.png)

## Telegraf Input Configuration

The following input plugin configuration is required to provide the data for these dashboards.

```
[[inputs.sensors]]
  # Remove numbers from field names. If true, a field name like 'temp1_input' will be changed to 'temp_input'.
  #remove_numbers = true

  # Timeout is the maximum amount of time that the sensors command can run.
  #timeout = "5s"
```
