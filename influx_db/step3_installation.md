Nun können wir mit der Installation beginnen.

# Download

Verwenden Sie diesen Befehl, um das InfluxDB v2.0 Docker image herunterzuladen und auszuführen.

`docker run -d --name influxdb -p 8086:8086 influxdb:2.0.4`{{execute}}

Weitere Möglichkeiten, mit denen InfluxDB auf MacOS, Linux oder in einem Kubernetes Cluster vewendet werden kann, finden Sie [hier](https://docs.influxdata.com/influxdb/v2.0/get-started/).

Damit später auf die im vorherigen Schritt angezeigte Datei verwendet werden kann, kopieren Sie sie mit diesem Befehl in den Ordner `data` im container.

`docker cp temperature-example.csv influxdb:/`{{execute}}

Um das InfluxDB Command Line Interface zu verwenden, öffnen Sie eine Konsole im Docker Container.

`docker exec -it influxdb /bin/bash`{{execute}}

# Setup

Um InfluxDB einzurichten, müssen einige Informationen bereitgestellt werden. Geben Sie dafür 'influx setup' ein und legen Sie ihre Einstellungen fest. Um anstattdessen Testdaten zu verwenden, führen Sie nur diesen Schritt aus und bestätigen Sie die Einstellungen mit `y`.

```
influx setup --username testname --password testpassword --org testorg --bucket testbucket --retention 0
```{{execute}}