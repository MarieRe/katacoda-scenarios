InfluxDB ist ein Produkt von [InfluxData](https://www.influxdata.com/). Die Zeitreihendatenbank wird Open-Source mit Go entwickelt und wurde 2013 erstmals veröffentlicht. Für die Verwendung von verwalteten InfluxDB-Clustern gibt es eine kostenlose, begrenzte Option und Vollversionen, die entweder nach Verwendung oder jährlich bezahlt werden. <sup>\[5\]</sup>

InfluxDB findet Anwendung in DevOps-Monitoring (z.B. bei IBM), für Real-Time Analytics (z.B. bei eBay) und in vielen weiteren Fällen. Stand 2016 ist InfluxDB die am häufigsten verwendete Zeitreihendatenbank. <sup>\[3\]</sup>

| **Vorteile**    | **Nachteile**   |
| --------------- | --------------- |
| Hoher Durchsatz (*read* und *write*) | Begrenzte Skalierbarkeit in Open-Source Version (kein Clustering) |
| Vielseitige Kompatibilität (Input plugins, Grafana, Programmiersprachen) | Eher kleine  (aber wachsende) Community |
| Schneller Einstieg durch gute Dokumentation und einfache Installation | Join-Operationen werden nicht unterstützt |
| Eigene SQL-ähnliche Abfragesprache (Continuous Queries werden unterstützt) | Gruppierung von Daten mit großen Abständen ist nicht möglich |
| Speicherzeit (retention) kann selbst festgelegt werden | nicht CRUD - *update* und *delete* ist nicht vorgesehen |

<sup>\[3\]</sup>

## Beispiel
Im Terminal sehen Sie die ersten 10 Reihen einer csv-Datei <sup>\[4\]</sup>, die die stündliche Temperatur in Stuttgart vom 1. bis zum 5. März 2021 zeigt.

![Temperaturverlauf](.\assets\temperature_example\temperature-graph.png)

Auf diesem Graph ist der Temperaturverlauf zu sehen. Zur Speicherung und Analyse dieser Zeitreihe bietet sich InfluxDB an.