Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in ihren erstellten bucket in InfluxDB.

```
influx write \
  --bucket testbucket \
  --url https://github.com/MarieRe/katacoda-scenarios/blob/1e45f3678990e37db383a8e3217074d0564deb80/influx_db/assets/temperature-example.csv
```{{execute}}
