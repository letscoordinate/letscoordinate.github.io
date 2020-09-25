# Let's Coordinate

## Requirements

* Maven
* Java 8
* Docker
* NPM (6 or grater) and Angular CLI (8 or grater)
* Linux (*Tested on Ubuntu v18.04 and Fedora 29*)
* Having Operator Fabric running ([https://opfab.github.io/documentation/current/getting_started/](https://opfab.github.io/documentation/current/getting_started/))

## Run Let's Co

Position yourself in the root directory of this project and run the following command:

`./bin/run_letscoos.sh`

This will start running the docker containers Kafka (*port 9092*), Zookeeper (*port 2181*), MariaDB (*port 3306*), the Let's Co data provider app. (*letsco-data-provider*) and the Let's Co main application (*letsco-api*).

#### Prepare the OperatorFabric environment

*1. Update the OpFab database*

Position yourself in the root directory of this project and run the following command:

`./test/prepare-opfab-env/prepare-opfab-env.sh`

This will create a new group, a new entity, and a new user associated to this group and this entity in the operator-fabric database, and send the bundles to display the cards in OperatorFabric.

*2. Add the user to keycloak*

- On your browser, go to the keycloak admin url: [http://localhost:89/auth/](http://localhost:89/auth/)
- Click on *Administration console*
- Connect using the following credentials: **user** *admin*, **password** *admin*
- In the left menu, go to *Users*
- Click on *Add user*
- Fill the **Username** field with *user.terna* and click on *Save*
- Go to *Credentials*
- Fill the password with whatever you want, put *Temporary* to *OFF* and click on *Reset Password*

#### Send a new notification

- Go to the following url: [http://localhost:8082/swagger-ui.html](http://localhost:8082/swagger-ui.html)
- Click on *kafka-producer-controller*
- Click on *POST /letsco/data-provider/v1/kafka/json/raw-msg*
- Click on *Try it out*
- In the data body value, put the content of one of the files from the directory `messages_models/json/card_feed/` (e.g: `MessageValidated_NEGATIVE_ACK.json`, `ProcessSuccess.json`)
- Click on *Execute*

If you connect to OpFab ([http://localhost:2002/ui/](http://localhost:2002/ui/)) with the user previously created in Keycloak, you should see the new card in the Feed.

#### generate an RSC KPI report

> **_NOTE:_** To be able to see the RSC KPI Report page, you should have the *letsco-front* module running! to do so, change directory to the *letsco-front* module and execute the command: `ng serve`

- Go to the following url: [http://localhost:8082/swagger-ui.html](http://localhost:8082/swagger-ui.html)
- Click on *kafka-producer-controller*
- Click on *POST /letsco/data-provider/v1/kafka/json/raw-msg*
- Click on *Try it out*
- In the data body value, put the content of the file `messages_models/json/rsc_kpi_report/kpi_use_cases.json`
- Click on *Execute*
- connect to OpFab ([http://localhost:2002/ui/](http://localhost:2002/ui/)) with the user previously created in Keycloak and then select the *"RSC KPI Report"* menu.
- select the *period*, *RSC*, *RSC Service* and *Data type* and then click the *submit* button, you should see the generated RSC KPI Report.

## Stop the application

Position yourself in the root directory of this project and run the following command:

`./bin/run_letscoos.sh stop`

This will stop the *letsco-api* & *letsco-data-provider* processes, and stop the docker services (*Kafka*, *Zookeeper*, *MariaDB*).
