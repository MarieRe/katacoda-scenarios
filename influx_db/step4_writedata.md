Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in ihren erstellten bucket in InfluxDB.

```
influx write \
  --bucket testbucket \
  --file temperature-example.csv
```{{execute}}
