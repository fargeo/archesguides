---
permalink: /admin-docs/collections/
layout: single
title: Collections
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
Collections are custom sets of concepts that are used in the dropdown lists and other suggested fields during data entry. Collections enable you to design your dropdown menus and give you greater control over how users will see the concept structure of your project. Thesauri are built by creating new concepts, whereas collections are created by adding existing concepts. A collection can be constructed from scratch or spawned from a thesaurus, and collections can have concepts added to them from multiple thesauri.
When designing a resource model, you will create some nodes that should only be set to certain values within a controlled vocabulary. For example, a node that denotes what state an address resides in might pull from a simple concept scheme that contains the names of the 50 states, which would ensure that the nodes value was always an actual state represented in consistent format. These types of nodes are set to the 'concept' datatype. Upon setting a node's datatype to 'concept', a 'Concept Collection' dropdown will appear that allows you to choose which collection that node will get its value from. When a user wants to enter a value for that node, they will be shown a dropdown with all the concepts contained in the concept collection set by the resource designer.

![Setting a collection]({{site.url}}/assets/GIFs/setCollection.gif)
