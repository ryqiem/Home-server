## Appdaemon

```bash
docker run --name=appdaemon -d -p 5050:5050 --restart=always -e HA_URL="http://192.168.1.150:8123" -e DASH_URL="http://$HOSTNAME:5050" -v /home/martin/docks/appdaemon/config:/conf -v /etc/localtime:/etc/localtime:ro acockburn/appdaemon:latest
```

Upgrading:

```bash
docker stop appdaemon
docker rm -f appdaemon
docker pull acockburn/appdaemon:latest
```

Then run the above