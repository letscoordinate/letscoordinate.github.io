<!-- Copyright (c) 2020 RTE (https://www.rte-france.com)                                                  -->
<!-- Copyright (c) 2020 RTE international (https://www.rte-international.com)                             -->
<!-- See AUTHORS.txt                                                                                      -->
<!-- This document is subject to the terms of the Creative Commons Attribution 4.0 International license. -->
<!-- If a copy of the license was not distributed with this                                               -->
<!-- file, You can obtain one at https://creativecommons.org/licenses/by/4.0/.                            -->
<!-- SPDX-License-Identifier: CC-BY-4.0                                                                   -->

# Version 1.0.0.RELEASE
---
<br/>

## 1. Features
{: .orange-title}

* Prepare generic JSON format
* Prepare generic Excel format
* Setup liquibase for database versioning
* Add letsco-data-provider module to read files from FTP server and send data to the backend
* Add API to transform valid Excel files to JSON and save generated data into database
* Initializing RSC KPI report module
* Add export RSC KPI Excel report functionality
* Add export RSC KPI PDF report functionality
* Setup Kafka to send cards to OpFab
* create process to send process successful card to OpFab
* create process to send process failed card to OpFab
* create process to send message validated card to OpFab
* Configure OpFab screens: card feed & archives
* Add online documentation: https://letscoordinate.github.io/
<br/>

## 2. Tasks
{: .orange-title}

* [LC-169] Allow a user to customize the title and summary in the feed for the card sent to opfab
* [LC-163] Make some screenshot for Let's Co OS + Sample of pdf/xlsx RSC KPI report
* [LC-162] Allow a user to customize a title and summary for the reduced view in opfab
* [LC-158] Add a README.md & tools that allows a new developer to run the project
* [LC-157] Implement the Excel download (RSC KPI report)
* [LC-156] Implement the PDF download (RSC KPI report)
* [LC-153] If specific message, send it to third app via POST call
* [LC-152] Add TSOs and RSCs config files
* [LC-149] Make a docker-compose or k8s quick deployment of letsco
* [LC-148] Create process to send message validated card to opfab
* [LC-147] Create process to send process failed card to opfab
* [LC-146] Create process to send process success card to opfab
* [LC-141] Create 2 excels files based on the 2 JSONs generic input files (ProcessFailed and ProcessSuccess)
* [LC-127] Send the JSONs
<br/>

## 3. Bugs
{: .orange-title}

* [LC-172] For all ACK negative notification, change the color of the notification in RED instead of orange
<br/>

## 4. Stories
{: .orange-title}

* [LC-17] Put all TSOs and RSCs list in a parameter list
<br/>
 