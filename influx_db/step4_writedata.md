Auflisten der Buckets - hier sehen sie den eben erstellten testbucket.

```
influx bucket list
``` {{execute}}

Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in den Bucket in InfluxDB.

```
influx write
    --bucket testbucket
    --header "#constant measurement,temperature"
    --header "#datatype dateTime:RFC3339,double"
    --file temperature-example.csv
```{{execute}}

Mit dem eben verwendeten `influx write`-Kommando können nicht nur Daten aus CSV-Dateien in einen InfluxDB-Bucket eingefügt werden, sondern auch aus dem Terminal oder aus einer URL.