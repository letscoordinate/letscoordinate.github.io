---
layout: page
title: Functional Design
permalink: /functional-design/
feature-img: "assets/img/blue-sky.jpg"
tags: [Doc, Functional Design]
---

# Executive Summary

This document describes detailed business specification of the Let’s Coordinate tool (Let's Co / Let’s Coordinate).
The main objective of this document is to ensure mutual detailed understanding on business functionality on the analytical level. The main goal is to guarantee that the requirements, processes, use-cases and their solution will be understood by all project parties.
The document focusses on detailed description of business functionalities, e.g. detailed description of the cards, format and content of output data and reports, description of flows or user interface of use-cases, etc.

Document covers:
- The main solution overview
- Detail description of general functionalities
- Detail description of logical data model
- Detail description of business processes
- Detail description of use cases
- Detail description of reports
- Detail description of output data

## Solution Overview

Let’s Coordinate is a cloud native platform developed for TSOs and RSCs.
It receives different informations from an external tool via a Kafka topic and displays them on the Let's Co app.: Positive ACKs, Negative ACKs, Merge results, etc.
It is currently developed for a large european organisation. The purpose of the platform is to provide to the user (TSO / RSC), in a pleasant manner, a way to follow the treatment of informations coming from the previously quoted external tools.

The following image shows the Let's Co process globally, from start to end:

![The Let's Co process, from start to end](../assets/img/letsco-process.svg "The Let's Co process, from start to end")

# General Functionalities

## Users
The following main user groups (business roles) shall be supported:
- TSO Users – Using Let’s Co from TSO point of view 
- RSC Users – Using Let’s Co from RSC point of view
- ___Administrators – System configuration and setting___

## Logging

All activities and events performed and carried out within the tool are subject to logging, which is based upon the following general principles:
- All the users working actively with the tool need to be logged in
- By the means of their user account, the extent of their user rights is defined
- Also, all their activities and actions within the tool are being logged in terms of what activity has been performed, who the responsible user is, with the date and of the respective action

## Screen size

Let's Coordinate is adapted for screens of size 1920x1080px.

# User Interface

## GUI Layout

This chapter describes the main screen layout and graphical user interface.
Layout consists of two main sections: Header Section and Main section.
Header Section keeps constant appearance across whole application. It contains navigation menu and other features that should be accessible independently on user’s role. Menu items are placed in unified structure. Feature set accessible by user depends on user’s access rights.  
Main Section contains the main use case functionality. Layout is specific per use case type but it always respects unified design language. This means:
- The use of colors is standardised
- The use of control elements, their locations and actions started by the elements are standardised
- A single function (such as OK button) does not have different meanings on different display views
- Data presented on the views are grouped into logical entities
- General information and error messages are displayed on constant location on page. Specific messages like validation errors can be displayed also near/at the particular input field (for example in edit screens). 

#### Navigation

All functionalities of Let’s Coordinate tool are accessible via the main application menu.  
___TODO description of the menu, its hierarchy and menu levels___

##### The Feed

On the feed, the user can see a list of his cards on the left of the screen. When he clicks on a card, the details of this card are then displayed on the right of the screen. The following image shows these two parts:  
___TODO image of the feed___

##### The Reporting
The user can consult a reporting, after selected a start date, an end date, and an RSC on which he wants this report.

#### Language

Let's Coordinate and all related materials are in English. 

# Business Processes

This chapter contains the detailed description of business processes in Let’s Co. Each business process is described in the next subchapters.
The table contains the business processes overview:

| Business process | Recipient | Card color |
| ---------------- | --------- | ---------- |
| Positive ACK | Concerned TSO (and its RSC) | Green |
| Negative ACK | Concerned TSO (and its RSC) | Orange |
| Merge results available | All TSOs and RSCs | Blue |
| TLI inconsistencies check | Concerned TSO (and its RSC) | Orange |
| Process failed | All TSOs and RSCs | Red |
| Adequacy results | All TSOs and RSCs | Blue |
| Reporting | Concerned user | / |

### Positive ACK

The recipient TSO (and its RSC) can consult a summary of this positive ACK in the form of a card in the Let’s Co app.
He can then forward this card to another user or aknowledge it.
Concerning the positive ACKs, the user can choose to not receive them, given that they are just informatives.

### Negative ACK

The recipient TSO (and its RSC) can consult a summary of this negative ACK in the form of a card in the Let’s Co app. 
The warnings and the errors are listed in this detailed card.
He can then forward it to another user or aknowledge it.
The user can choose to not see the warnings if he wants to just see the errors.

### Merge results available

All TSOs and RSCs receive these informations in the form of a card in the Let’s Co app. 
The user can then download these results in the xlsx format.

### TLI Inconsistencies check

The recipient TSO (and its RSC) can consult a summary of these TLI inconsistencies check in the form of a card in the Let’s Co app. 
He can then forward this card to another user or aknowledge it.

### Process failed

The recipient TSO (and its RSC) can consult a summary of this failed process in the form of a card in the Let’s Co app. 
He can then forward this card to another user or aknowledge it.

### Adequacy results

All TSOs and RSCs can consult a report of the adequacy results in the form of a card in the Let’s Co app. 
The deterministic results and the probabilistic results are viewable on two separated tables.
They can then download these reports on a pdf or an xml format.

### Reporting

The user (TSO or RSC) chooses:
- a starting date
- an end date
- an RSC (or "all RSCs")

and can then consult a reporting on this time interval.
He can download this reporting on a PDF/xlsx format.

# _Revision History_

| Version | Date | Author
| ------- | ---- | ------
| 00.01 | 18/02/19 | CHEHADE Sami