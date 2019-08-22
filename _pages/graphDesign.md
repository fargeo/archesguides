---
permalink: /admin-docs/graph-design/
layout: single
title: Graph
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
The Graph tab is where you design the structure of your resource model. From here you can add child nodes under the top node. The first level of children nodes will usually be semantic nodes because nodes with the semantic data type define a NodeGroup. Under these first level semantic nodes you can add children nodes of any datatype to create a set of attributes that will be contained in the NodeGroup. You can create as many levels of nesting NodeGroups as you want by adding semantic nodes under a NodeGroups existing semantic node.  ![Example of Nested NodeGroups]({{site.url}}/assets/images/nestedNodegroupsAnnotated.png) In this example, 'Production' is a semantic node whose NodeGroup contains some non-semantic nodes which hold data as well as the semantic node 'Assets', which forms its own NodeGroup. The 'Assets' NodeGroup has a non-semantic 'Asset Type' node and another semantic node which forms a 'Material' node group. You can see how nesting NodeGroups helps categorize data and is necessary for creating a comprehendible resource model.
