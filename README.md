# PRETTYFLY

## Pre-Deployment

1. Check if any new Home Assistant entities require adding to Influxdb

## Deployment

1. Git clone pretty-fly-docker

2. Check new config files are added to repo

3. Deploy secret & environment files using script

```bash
influxdb/influxdbsecrets.env
mqtt/sec/secfile
telegraf/telegrafsecrets.env
homeassistant/config/secrets.yaml
homeassistant/config/ha.env
.env

To be added:
nodered/.config.json
```
###MQTT
4. Create mosquitto.log file

###NODE_RED
5. Change NODE_RED owner to 1001:1001 (sudo chown -R 1001:1001 node-red)

6. Pull nodered repo from git using nodered key

###GRAFANA
7. Set grafana password as per local

###influxdb
8. Create homeassistant db
  - Influxdb CLI command
```bash
  influx -precision rfc3339
  CREATE DATABASE homeassistant
```

###HOMEASSISTANT
7. Setup creds as per note

8. Check that InfluxDB



X. Check which MQTT broker HASS is connected to

TO DO:
- HA logging levels
- InfluxDB retention, CQ and config
- System monitor in docker (volume mapping)
- Update HACS store
- Change packages structure
- Add Alexa TTS
