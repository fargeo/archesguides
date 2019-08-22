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
The Graph tab is where you design the structure of your resource model. From here you can add child nodes under the top node. The first level of children nodes will usually be semantic nodes because nodes with the semantic data type define a NodeGroup. Under these first level semantic nodes you can add children nodes of any datatype to create a set of attributes that will be contained in the NodeGroup. You can create as many levels of nesting NodeGroups as you want by adding semantic nodes under a NodeGroups existing semantic node.  ![Example of Nested NodeGroups]({{site.url}}/assets/images/nestedNodegroupsAnnotated.png) 

**In this example you can see:**
- A semantic type 'Production' node forming a NodeGroup
- A semantic type 'Assets' node that forms a NodeGroup within 'Production'
- A semantic type 'Material' node that forms a NodeGroup within 'Assets'
- Nodes of other types within each NodeGroup that hold data (non-semantic)
