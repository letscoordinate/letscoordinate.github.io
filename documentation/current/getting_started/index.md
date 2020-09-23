# Let's Coordinate

## Requirements

* Maven
* Java 8
* Docker
* Linux (*Tested on Ubuntu v18.04 and Fedora 29*)
* Having Operator Fabric running (*https://opfab.github.io/documentation/current/getting_started/*)

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

- On your browser, go to the keycloak admin url: http://localhost:89/auth/
- Click on *Administration console*
- Connect using the following credentials: **user** *admin*, **password** *admin*
- In the left menu, go to *Users*
- Click on *Add user*
- Fill the **Username** field with *user.terna* and click on *Save*
- Go to *Credentials*
- Fill the password with whatever you want, put *Temporary* to *OFF* and click on *Reset Password*

#### Send a new notification

- Go to the following url: http://localhost:8082/swagger-ui.html
- Click on *kafka-producer-controller*
- Click on *POST /letsco/data-provider/v1/kafka/json/raw-msg*
- Click on *Try it out*
- Put in the data body value the content of the file *messages_models/jsons/Anonymised_JSONs/MessageValidated_NEGATIVE_ACK_v0.2_oneline.json*
- Click on *Execute*

If you connect to OpFab (http://localhost:2002/ui/) with the user previously created in Keycloak, you should see the new card in the Feed.


## Stop the application

Position yourself in the root directory of this project and run the following command:

`./bin/run_letscoos.sh stop`

This will stop the *letsco-api* & *letsco-data-provider* processes, and stop the docker services (*Kafka*, *Zookeeper*, *MariaDB*).
