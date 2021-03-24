Um zu überprüfen, ob der Schreibvorgang erfolgreich war, führen Sie die erste Abfrage aus: 

`from(bucket:"testbucket") |> range(start: 2021-03-01T10:00:00Z, stop: 2021-03-01T20:00:00Z)`{{execute}}