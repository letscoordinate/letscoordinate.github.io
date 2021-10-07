<!-- Copyright (c) 2020-2021 RTE (https://www.rte-france.com)                                                  -->
<!-- Copyright (c) 2020-2021 RTE international (https://www.rte-international.com)                             -->
<!-- See AUTHORS.txt                                                                                      -->
<!-- This document is subject to the terms of the Creative Commons Attribution 4.0 International license. -->
<!-- If a copy of the license was not distributed with this                                               -->
<!-- file, You can obtain one at https://creativecommons.org/licenses/by/4.0/.                            -->
<!-- SPDX-License-Identifier: CC-BY-4.0                                                                   -->

# Version 1.3.1.RELEASE
---
<br/>

## 1. Features
{: .orange-title}

* Add the LTTD (Last Time To Decide) feature to Smart notifications: Coordination use case
* Improve the export in the "Monitoring" screen
* Improve the "RSC KPI report" screen
* Remove of the "letsco-data-provider" module
* Upgrade the OperatorFabric dependencies to version 2.10.0.RELEASE
* Update the online documentation of Let's Coordinate 1.3.1.RELEASE

## 2. Tasks
{: .orange-title}

* [LC-461] RSC KPIs - No data for selected filter (granularity, RSC, CCR)
* [LC-756] Integrate the Last Time To Decide (LTTD) use case
* [LC-806] Refactoring of ObjectMapper config (serializer/deserializer) to be used by third applications
* [LC-874] Upgrade of Keycloak to version 12.0.4
* [LC-883] Remove letsco-data-provider module
* [LC-893] Customization of the monitoring export file
* [LC-900] Upgrade the version of OperatorFabric to 2.10.0.RELEASE
* [LC-908] Hide coordination file cards from notif reception config screen and from feed
* [LC-941] Add Coordination B bundle with LTTD disabled
* [LC-942] Scan code with Fossology
* [LC-943] Update documentation for Letsco OS 1.3.1

## 3. Bugs
{: .orange-title}

* [LC-809] Fix services update issue in RSC KPI config screen
* [LC-823] Result card should be sent after LTTD expiration even if all users answered
* [LC-880] Fix docker images names
* [LC-882] Free messages are not sent to any user
* [LC-899] Increase filename column size to 1000
* [LC-907] Coordination card not correctly displayed in archive screen
* [LC-922] Change the dates format in generated caseId to epoch milliseconds format