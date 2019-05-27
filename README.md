# PRETTYFLY

## Deployment

1. Git clone pretty-fly-docker

2. Check new config files are added to repo

3. Deploy secret & environment files using script

```bash
influxdb/influxdbsecrets.env
mqtt/sec/secfile
telegraf/telegrafsecrets.env
homeassistant/config/secrets.yaml
.env

To be added:
nodered/.config.json
```
###MQTT
4. Create mosquitto.log file

###NODE_RED
5. Change NODE_RED owner to 1001:1001 (sudo chown -R 1001:1001 node-red)

6. Pull nodered repo from git using nodered key

###HOMEASSISTANT
7. Setup creds as per note


X. Check which MQTT broker HASS is connected to
