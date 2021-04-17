Um zu überprüfen, ob der Schreibvorgang erfolgreich war, führen Sie die erste Abfrage aus: 

```
influx query 'from(bucket:"testbucket")
    |> range(start: 2021-03-01T10:00:00Z, stop: 2021-03-01T20:00:00Z)
    |> drop(columns: ["_start", "_stop"])'
```{{execute}}

Mit dem Kommando `influx query` können [Flux](https://docs.influxdata.com/influxdb/cloud/reference/flux/)-Abfragen in InfluxDB ausgeführt werden. Für simple Abfragen wird ein Bucket und ein Zeitraum (`range`) angegeben, die Ergebnisse können aber auch noch weiter eingeschränkt werden. Für bessere Übersichtlichkeit werden die automatisch zur Abfrage generierten Spalten "_start" und "_stop" mit dem Befehl `drop` aus dem Ergebnis entfernt. Durch die Flag `--raw` können die Ergebnisse als csv exportiert werden.

Mit der folgenden Abfrage können wir den Median dieses Zeitraums abfragen. Weitere Befehle finden Sie [hier](https://docs.influxdata.com/influxdb/cloud/query-data/flux/).
```
influx query 'from(bucket:"testbucket")
    |> range(start: 2021-03-01T10:00:00Z, stop: 2021-03-01T20:00:00Z)
    |> drop(columns: ["_field", "_measurement"])
    |> median()'
```{{execute}}

Nutzen Sie dieses Environment gerne, um weitere Befehle auszuprobieren! Können Sie beispielsweise die wärmste Stunde des 2. März 2021 herausfinden? _Bei Schwierigkeiten finden Sie im nächsten Schritt einen Tipp._