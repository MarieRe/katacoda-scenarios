Allgemein betrachtet werden Zeitreihendatenbanken wie InfluxDB verwendet, um Daten zu speichern, denen jeweils ein spezifischer Zeitstempel zugeordnet ist.  
In den meisten Fällen werden Daten in gleichmäßigen Abständen erhoben, so dass eine diskrete Zeitreihe entsteht. Die Daten werden zur Auswertung im zeitlichen Verlauf betrachtet und auf Muster untersucht. Wenn Daten als Diagramm mit dem zeitlichen Verlauf auf der x-Achse dargestellt werden ist dies ein klares Indiz dafür, dass Zeitreihendatenbanken eine gute Wahl sein könnten. <sup>\[4\]</sup>

### Anwendung
Ein typischer Anwendungsfall ist die Erhebung von Sensordaten in einer IoT-Umgebung. In festgelegten Abständen, beispielsweise sekündlich, werden Messdaten gewonnen, die mit Zeitstempel festgehalten und in ihrer zeitlichen Entwicklung ausgewertet werden.  
Durch den Einsatz von Zeitreihendatenbanken wird eine sinnvolle und einfache Auswertung dieser Daten ermöglicht. Zusätzlich zur Beobachtung der Veränderung von Variablen im Lauf der Zeit kann es möglich sein, durch den Einsatz von Machine Learning die weitere Entwicklung vorherzusagen. Außerdem können mehrere Zeitreihen in Kontext gesetzt werden, um mögliche Korrelationen zu entdecken. <sup>\[2\]</sup>

## Anforderungen

Wichtige Anforderungen für Zeitreihendatenbanken sind unter anderem: <sup>\[3\]</sup>
- **Hohe Performance** für Schreibvorgänge und Abfragen, da in kurzen Abständen viele Daten hinzugefügt werden
- **Datenkomprimierung** muss möglich sein, da kleine Unterschiede unwichtiger werden, je älter die Daten sind
- **Skalierbarkeit**, da meist große Datenmengen in kurzer Zeit produziert werden
