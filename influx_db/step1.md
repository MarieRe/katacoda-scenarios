<!-- A Katacoda scenario is a series of Markdown files, bash scripts and a JSON file to define how your scenario should be configured, the text for the scenario and any automation required.

## Task

Clone our example repository that contains the set of documentation with the following command:

`git clone https://github.com/katacoda/scenario-examples.git katacoda-scenario-examples`{{execute}}

Within the repository, you will see a set of examples of implementing various Katacoda functionality.

The scenario you are currently reading is in the directory `ls -lha katacoda-scenario-examples/create-scenario-101`{{execute}}. The directory name is what defines the URL.

An example of the current step is `katacoda-scenario-examples/create-scenario-101/step1.md`{{open}}

All the steps are collected via a JSON file, for example, `katacoda-scenario-examples/create-scenario-101/index.json`{{open}}.

The JSON file defines the scenario title, the description, steps order, the UI layout and environment. You can find more about the layouts within our scenarios at [katacoda.com/docs/scenarios/layouts](https://katacoda.com/docs/scenarios/layouts) and environments at [katacoda.com/docs/scenarios/environments](https://katacoda.com/docs/scenarios/environments). -->

InfluxDB bla bla bla

# Download

Verwenden Sie diesen Befehl, um das InfluxDB v2.0 Docker image herunterzuladen und auszuführen.

`docker run -d --name influxdb -p 8086:8086 influxdb:2.0.4`{{execute}}

Weitere Möglichkeiten, mit denen InfluxDB auf MacOS, Linux oder in einem Kubernetes Cluster vewendet werden kann, finden Sie hier: https://docs.influxdata.com/influxdb/v2.0/get-started/

Um das InfluxDB Command Line Interface zu verwenden, öffnen Sie eine Konsole im Docker Container.

`docker exec -it influxdb /bin/bash`{{execute}}

# Setup

Um InfluxDB einzurichten, müssen einige Informationen bereitgestellt werden. Geben Sie dafür 'influx setup' ein und legen Sie ihre Einstellungen fest. Um anstattdessen Testdaten zu verwenden, führen Sie nur diesen Schritt aus:

```
influx setup
    --username testname
    --password testpassword
    --org testorg
    --bucket testbucket
```{{execute}}