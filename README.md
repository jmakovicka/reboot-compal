Watchdog utility for Compal CH7465LG routers
============================================

This is a crude but working utility that pings predefined hosts, and
if none of them is reachable, it reboots the (presumably stuck)
router. It can be launched periodically from cron.

It's tested on the "UPC Connect Box" router distributed in the Czech
Republic.

Example usage:

```
reboot-compal-if-needed --router-password f00bar12345 --ping-host upc.cz
```

The `--ping-host` option can be specified multiple times to avoid
reboots if one particular host goes down.
