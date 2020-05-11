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
- InfluxDB retention, CQ and config
- System monitor in docker (volume mapping)
- Change packages structure
- Add Alexa TTS
- Update synology secrets
- Complete PING file
- Remove unwanted sensors from recorder - Last boot
- Add Yale
- Add trains
- Add location
- Update Sonoff RF Sensor
- timer

title: Timer
 card:
   type: "custom:button-card"
   entity: sensor.mark_s_echo_dot_next_timer
   show_state: true
   show_name: false
   color_type: card
   color_off: rgb(218, 108, 108)
   action: more-info
   style:
    font-size: 140px
    font-weight: bold
   styles:
     state:
       - font-size: 180px
     card:
       - width: 1200px
       - height: 600px
 deviceID:
   - e3c5cf9d-8b56827e
 large: true
