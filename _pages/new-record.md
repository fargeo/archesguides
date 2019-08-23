---
permalink: /user-docs/new-record/
layout: single
title: Creating a New Record
sidebar:
  nav: "user docs"
toc: true
toc_label: "Table of Contents"
toc_icon: "file-alt"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---

To create a new record, go to the "Add New Resource" tab and select the resource model that best fits for the record you want to create.
![Create Record]({{site.url}}/assets/images/newRecordAnnotated.png)

# Resource Structure
Once you have selected a resource model, your record will be displayed as a card tree on the left hand side.  
![Card Tree]({{site.url}}/assets/images/cardTreeAnnotated.png)  

You can think of creating data within your record as adding cards. Some cards are nested within other cards to give more structure to records.
## Branches
Branches are a non-editable version of a resource model that can be used in multiple records and types of resources. Branches allow you to reuse complex node structures across multiple records.
## Cards
Each field that data can be entered into on a card is a node that can be set to a value depending on its datatype.
### Adding a Record
To add a record:
1. Select any card that you want to add data to
1. Fill out any of the fields on the card that you have data for, some cards have required fields that you must enter a value for in order to create the card
1. Click the ![Add Button]({{site.url}}/assets/images/addButton.png) button
### Saving a Record
To save a Record:
1. Select any already created card that has data you want to edit or that you want to add new data to
1. Change any information that needs editing and fill out any of the empty fields you wish to add data for
1. Click the ![Save Edit Button]({{site.url}}/assets/images/saveEditButton.png)
# Approval Process
Depending on what user groups you're in and what your project administrators have set your permissions to, your edits may show up as 'Provisional' when you first make them.  
![Provisional Edit in Search]({{site.url}}/assets/images/provEdit.png)
To maintain the integrity of a projects database, Arches has a built in quality assurance system that allows a set group of resource reviewers to examine provisional edits and then approve or decline them.
![Provisional Edit in Search]({{site.url}}/assets/images/provReview.png)
