Auflisten der Buckets - hier sehen sie den eben erstellten testbucket.

```
influx bucket list
``` {{execute}}

Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in ihren erstellten Bucket in InfluxDB.

```
influx write\
    --bucket testbucket\
    --header "#constant measurement,temperature"\
    --header "#datatype dateTime:RFC3339,double"\
    --file temperature-example.csv
```{{execute}}
