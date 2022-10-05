# IOT environment with Mosquitto/InfluxDB/Grafana

Use `docker-compose up --build` to start the environment.
Once started, Go to [InfluxDB web interface](http://localhost:8086/) use `admin`/`admin` creadential, set admin password. Create a new user ad get its token. It will be used in Telegraf (for feeding) and in Grafana (consuming). fix token in `config/telegraf.conf`.
# Services provided by Docker:
 - Mosquitto
   - MQTT 1883
   - MQTT/TLS 9001
 - InfluxDB 
   - API  8083
   - Admin 8086
6- Grafana
   - Web interface : 3000
