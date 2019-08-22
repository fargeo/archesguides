---
permalink: /admin-docs/models/
layout: single
title: Configuring Models
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
Model configuration is done from the Arches designer tab. If you loaded a package into your Arches instance, you probably already have a handful of resource models that can be viewed and edited from here. To add a new resource model to this list, simply select 'New Resource Model' from the Add button in the upper right. Clicking on an existing resource model or creating your own will bring up the Arches designer interface with the selected model's graph tree on the left (it will contain only a top node when first creating a new model). The Arches designer is separated into three sections (Graph, Cards, and Permissions) each of which manages a different aspect of designing resource models.
![Creating a new resource model]({{site.url}}/assets/GIFs/modelCreate.gif)
# Graph
The Graph tab is where you design the structure of your resource model. From here you can add child nodes under the top node. The first level of children nodes will usually be semantic nodes because nodes with the semantic data type define a NodeGroup. Under these first level semantic nodes you can add children nodes of any datatype to create a set of attributes that will be contained in the NodeGroup.

# Cards
User interface is controlled from the cards tab. The node structure of your resource model will be shown by the card tree on the left. Each NodeGroup defined by a semantic node makes up one card. Each node in a NodeGroup is controlled by a widget on that NodeGroups card. You can click on a semantic node to view the card for its NodeGroup, or click on a node to jump to its card and select its widget.

# Permissions
From the Permissions tab you can control the viewing and editing privileges of each user group. Permissions are set at the card level, so only the semantic nodes that form NodeGroups are selectable from the Permissions tab.
