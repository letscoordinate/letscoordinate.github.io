<!-- Copyright (c) 2020-2021 RTE (https://www.rte-france.com)                                                  -->
<!-- Copyright (c) 2020-2021 RTE international (https://www.rte-international.com)                             -->
<!-- See AUTHORS.txt                                                                                      -->
<!-- This document is subject to the terms of the Creative Commons Attribution 4.0 International license. -->
<!-- If a copy of the license was not distributed with this                                               -->
<!-- file, You can obtain one at https://creativecommons.org/licenses/by/4.0/.                            -->
<!-- SPDX-License-Identifier: CC-BY-4.0                                                                   -->

# Version 1.3.0.RELEASE
---
<br/>

## 1. Features
{: .orange-title}

* Add new functionalities: 
    * Add "Smart notification" concept: Coordination use case 
    * Add "Monitoring" screen
    * Add "Logging" screen
* Update the JSON generic input/output format
* Upgrade the OperatorFabric dependencies to version 2.8.0.RELEASE
* Improve the getting started process and documentation
* Update the online documentation of Let's Coordinate 1.3.0.RELEASE
<br/>

## 2. Epics
{: .orange-title}

* [LC-647]	LetsCo OS Coordination 1.3.0

## 3. Tasks
{: .orange-title}

* [LC-235] Create a SMART notification to validate a generic proposal
* [LC-236] NOT1 - SMART Notification asking a choice for the concerned TSO (1 validation required)
* [LC-237] NOT1 - SMART Notification asking a choice for the concerned TSO (2 or more validations required)
* [LC-486] Allow the value field in the timeseries details data to be null
* [LC-529] Display Logging and Monitoring screens
* [LC-567] Save original input file and generate unique file identifier
* [LC-568] Generate output file for generic messages
* [LC-569] Create APIs to manage specific messages output files by third applications
* [LC-677] Display the coordination's input and output files in the logging screen
* [LC-705] Upgrade the version of OperatorFabric to 2.8.0.RELEASE
* [LC-707] Make configurable the auto generation of the unique case id
* [LC-715] Update documentation for Letsco OS 1.3.0
* [LC-729] Scan code with Fossology
<br/>

## 4. Bugs
{: .orange-title}

* [LC-564] Fix the TSOs names in the Smart notification
* [LC-708] Coordination result card is no longer displayed since OpFab v2.8.0