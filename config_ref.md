# ESM_Healthmon Configuration Reference

Configuration file is "healthmon.ini". This configuration file is automatically generated with:
```awk
python healthmon.py config
```
If there is an existing healthmon.ini file you will be prompted before it is overwritten.

## healthmon.ini Format
The file must start with the section `[healthmon]`. # is used for comments. 

## healthmon.ini Options
|Option|Description|Values|Default|
| --- | --- | --- | --- |
|monitor_alarms|Enable or disable alarm monitoring. |true or false|Default: true|
|alarm_window|Time range in which to query for alarms|ESM Timerange*|Default: LAST_HOUR|
|alarm_threshold|Age limit in minutes of an alarm before reporting a problem|Default: 30|
|monitor_queries|Enable or disable query monitoring.|true or false|Default: true|
|event_window|Time range in which to query for events|ESM_Timerange*|Default: LAST_HOUR
|query_* |Options that start with `query` designate a device to query. Following the `query` prefix is a unique but arbitary name for the device. (e.g. query_erc3). The value is the device ID to query followed by the idle threshold in minutes.

### *ESM Timeranges
ESM Timeranges are listed below for reference. In almost all cases, LAST_HOUR is the best time range to use.

    LAST_MINUTE
    LAST_10_MINUTES
    LAST_30_MINUTES
    LAST_HOUR
    CURRENT_DAY
    PREVIOUS_DAY
    LAST_24_HOURS
    LAST_2_DAYS
    LAST_3_DAYS
    CURRENT_WEEK
    PREVIOUS_WEEK
    CURRENT_MONTH
    PREVIOUS_MONTH
    CURRENT_QUARTER
    PREVIOUS_QUARTER
    CURRENT_YEAR
    PREVIOUS_YEAR
