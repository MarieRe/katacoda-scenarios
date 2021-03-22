Allgemein betrachtet werden Zeitreihendatenbanken wie InfluxDB verwendet, um Daten zu speichern, denen jeweils ein spezifischer Zeitstempel zugeordnet ist.  
In den meisten Fällen werden Daten in gleichmäßigen Abständen erhoben, so dass eine diskrete Zeitreihe entsteht. Die Daten werden zur Auswertung im zeitlichen Verlauf betrachtet und auf Muster untersucht. Wenn Daten als Diagramm mit dem zeitlichen Verlauf auf der x-Achse dargestellt werden ist dies ein klares Indiz dafür, dass Zeitreihendatenbanken eine gute Wahl sein könnten.

### Anwendung
Ein typischer Anwendungsfall ist die Erhebung von Sensordaten in einer IoT-Umgebung. In festgelegten Abständen, beispielsweise sekündlich, werden Messdaten gewonnen, die mit Zeitstempel festgehalten und in ihrer zeitlichen Entwicklung ausgewertet werden.  
Durch den Einsatz von Zeitreihendatenbanken wird eine sinnvolle und einfache Auswertung dieser Daten ermöglicht. Zusätzlich zur Beobachtung der Veränderung von Variablen im Lauf der Zeit kann es möglich sein, durch den Einsatz von Machine Learning die weitere Entwicklung vorherzusagen. Außerdem können mehrere Zeitreihen in Kontext gesetzt werden, um mögliche Korrelationen zu entdecken.

## Anforderungen

Wichtige Anforderungen für Zeitreihendatenbanken sind unter anderem:
- **Hohe Performance** für Schreibvorgänge und Abfragen, da in kurzen Abständen viele Daten hinzugefügt werden
- **Datenkomprimierung** muss möglich sein, da kleine Unterschiede unwichtiger werden, je älter die Daten sind
- **Skalierbarkeit**, da meist große Datenmengen in kurzer Zeit produziert werden

## Beispiel
Im Terminal sehen Sie die ersten 10 Reihen einer csv-Datei, die die Abweichung der durchschnittlichen Jahrestemperatur (1916-2016) vom Durchschnitt des gesamten 20. Jahrhunderts zeigt.

![Graph](assets\temperature_graph.PNG)

Auf diesem Graph ist der Temperaturverlauf zu sehen. Zur Speicherung und Analyse dieser Zeitreihe bietet sich InfluxDB an.

&nbsp;

**Abkürzungen:**  
IoT - Internet of Things

**Quellen:**
- Joshi, P., Hearty, J., Sjardin, B., Massaron, L. & Boschetti, A. (2016). Python : real world machine learning : learn to solve challenging data science problems by building powerful machine learning models using Python. Birmingham, UK: Packt Publishing
- Namiot, D. (2015). Time Series Databases. DAMDID/RCDL, 1536, 132-137.
- Naqvi, S. N. Z., Yfantidou, S., & Zimányi, E. (2017). Time series databases and influxdb. Studienarbeit, Université Libre de Bruxelles, 12.
- https://datahub.io/core/global-temp/r/0.html
