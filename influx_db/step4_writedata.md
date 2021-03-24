Auflisten der Buckets - hier sehen sie den eben erstellten testbucket.

```
influx bucket list
``` {{execute}}

Wechseln sie in den Ordner `data` und zeigen sich die Dateien an.

```
cd data
ls
```{{execute}}

Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in ihren erstellten Bucket in InfluxDB.

```
influx write \
  --bucket testbucket \
  --file temperature_example.csv
```{{execute}}
