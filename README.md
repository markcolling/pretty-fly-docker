# PRETTYFLY

## Deployment

1. Check new config files are added to repo

2. Manually deploy secret & environment files

```bash
influxdb/influxdbsecrets.
mqtt/sec/secfile
telegraf/telegrafsecrets.env
homeassistant/config/secrets.yaml
.env
```

3. Check which MQTT broker HASS is connected to


TO DO:
Sort nodered .gitignore and project git out
Ensure all folders used as volumes are included in git
