<!-- Copyright (c) 2020-2021 RTE (https://www.rte-france.com)                                                  -->
<!-- Copyright (c) 2020-2021 RTE international (https://www.rte-international.com)                             -->
<!-- See AUTHORS.txt                                                                                      -->
<!-- This document is subject to the terms of the Creative Commons Attribution 4.0 International license. -->
<!-- If a copy of the license was not distributed with this                                               -->
<!-- file, You can obtain one at https://creativecommons.org/licenses/by/4.0/.                            -->
<!-- SPDX-License-Identifier: CC-BY-4.0                                                                   -->

# Version 1.2.0.RELEASE
---
<br/>

## 1. Features
{: .orange-title}

* Add new functionalities: 
    * Add "Card creation" screen
    * Add "Notification reception configuration" screen
* Update existing functionalities:
    * "Card feed" screen:
        * Display multiple bubbles in timeline for notifications with errors and/or warnings
    * "Archives" screen:
        * Update filtering tags
        * Add export functionality
    * "RSC KPI report" screen:
        * Add yearly granularity
        * Add regional selection
        * Add new graph types
* Update the JSON generic format
* Make Let's Coordinate compatible with the version 2.3.0.RELEASE of OperatorFabric
* Improve the getting started process and documentation
* Improve the security of the Let's Coordinate application
* Improve the code quality by integrating the Sonar tool
* Update online documentation for release 1.2.0.RELEASE
<br/>

## 2. Tasks
{: .orange-title}

* [LC-208] Display many bubbles in timeline for notifications that have errors and warnings
* [LC-242] Add yearly view and region concept to RSC KPI report
* [LC-408] Upgrade the version of OperatorFabric to 2.3.0.RELEASE
* [LC-258] Integrate the "Card creation" screen
* [LC-262] Integrate the "Notification Reception Configuration" screen
* [LC-189] Improve the getting started process and documentation
* [LC-191] Improve the security of the backend and frontend modules 
* [LC-254] Change rules for displaying cards in feed 
* [LC-255] Split validation tags in the archive screen 
* [LC-256] Change National Grid's EIC Code
* [LC-260] Improve the validator of JSON and Excel files
* [LC-264] Split granularity and period selection in RSC KPI config screen
* [LC-267] Add new fields to the JSON generic format and update the implementation guide
* [LC-284] Specify the list of messageTypeNames recognized by the letsco API
* [LC-285] Upgrade Letsco OS frameworks
* [LC-287] Update TSOs, RSCs and regions mapping
* [LC-316] Use joinGraph attribute for joining RSC KPI graphs
* [LC-333] Improve the authentication for the RSC KPi report screen
* [LC-371] Change RSC KPI bar graphs to stacked bar graphs when joinGraph flag equals true
* [LC-378] Update CCRs/Regions EicCodes
* [LC-150] Integrate sonar to check the test coverage
* [LC-363] Scan code with Fossology
* [LC-403] Add unit tests 
<br/>

## 3. Bugs
{: .orange-title}

* [LC-350] Fix VPN/Proxy access problems
* [LC-373] Fix the publisher name displayed on the bottom of the free message card details
* [LC-315] Fix tags in the archive screen
* [LC-209] Identify fields that may have long values and increase their size in database
