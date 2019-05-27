# PRETTYFLY

## Deployment

1. Git clone pretty-fly-docker

2. Git clone pretty-fly-node-red

git clone https://github.com/markcolling/pretty-fly-nodered.git

3. Check new config files are added to repo

4. Deploy secret & environment files using script

```bash
influxdb/influxdbsecrets.env
mqtt/sec/secfile
telegraf/telegrafsecrets.env
homeassistant/config/secrets.yaml
.env
```
5. Create mosquitto.log file

6. Change NODE_RED permissions (find . -type d -exec chmod 777 {} \;)

X. Check which MQTT broker HASS is connected to


TO DO:
Sort nodered .gitignore and project git out
Ensure all folders used as volumes are included in git
