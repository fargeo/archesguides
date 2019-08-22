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
The Arches designer is separated into three sections that each manage a different aspect of designing resource models.

# Graph
The Graph tab is where you design the structure of your resource model. From here you can add child nodes under the top node. This first level of children nodes will usually be semantic nodes because nodes with the semantic data type define a NodeGroup. Under these first level semantic nodes you can add children nodes of any datatype to create a set of attributes that will be contained in the NodeGroup.

# Cards
User interface is controlled from the cards tab. The node structure of your resource model will be shown by the card tree on the left. Each NodeGroup defined by a semantic node makes up one card. Each node in a NodeGroup is controlled by a widget on that NodeGroups card. You can click on a semantic node to view the card for its NodeGroup, or click on a node to jump to its card and select its widget.
# Permissions
