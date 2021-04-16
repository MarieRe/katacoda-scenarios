Auflisten der Buckets - hier sehen sie den eben erstellten testbucket.

```
influx bucket list
``` {{execute}}

Nutzen Sie die bereitgestellte csv-Datei und schreiben Sie die Daten in den Bucket in InfluxDB.

```
influx write \
    --bucket testbucket \
    --header "#constant measurement,temperature" \
    --header "#datatype dateTime:RFC3339,double" \
    --file temperature-example.csv
```{{execute}}

Mit dem eben verwendeten `influx write`-Kommando können nicht nur Daten aus CSV-Dateien in einen InfluxDB-Bucket eingefügt werden, sondern auch aus dem Terminal oder aus einer URL.

Mit dem Kommando `influx delete` können Datenpunkte innerhalb eines Zeitraums aus einem Bucket entfernt werden.

```
influx delete \
    --bucket example-bucket \
    --start 2021-03-04T20:00:00Z \
    --stop 2021-03-05T00:00:00Z
```{{execute}}

Ein dedizierter `update`-Befehl existiert für InfluxDB nicht, denn das Einfügen eines Eintrags mit einem existierenden Zeitstempel überschreibt den bisherigen Eintrag mit diesem Zeitstempel. In den meisten Anwendungsfällem von InfluxDB, wie Sensordaten, ist das Updaten auch nicht vorgesehen, da die Zeitdaten erzeugt und im Anschluss nicht mehr verändert werden, sondern nur noch ausgewertet. Damit beschäftigt sich diese Einführung im nächsten Kapitel.