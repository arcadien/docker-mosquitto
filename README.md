# IOT environment with Mosquitto/InfluxDB/Grafana

Use `docker-compose up --build` to start the environment.
Once started, Go to [InfluxDB admin interface](http://localhost:8086/) use `admin`/`admin` creadential, set admin password. Create a new user ad get its token. It will be used in Telegraf (for feeding) and in Grafana (consuming). fix token in `config/telegraf.conf`.
## Services provided by Docker:

Mosquitto (MQTT broker) => Telegraf (data adapter) -> InfluxDB (data store) -> Grafana (data display)

 - Mosquitto
   - MQTT at localhost:1883
   - HTTP/Websocket at localhost:9001
 - InfluxDB
   - Web interface at http://locahost:8086
 - Grafana
   - Web interface at http://locahost:3000
