---
permalink: /admin-docs/model-structure/
layout: single
title: Model Structure
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
Model configuration is done from the Arches designer tab. If you loaded a package into your Arches instance, you probably already have a handful of resource models that can be viewed and edited from here. To add a new resource model to this list, simply select 'New Resource Model' from the Add button in the upper right.  

![Creating a new resource model]({{site.url}}/assets/GIFs/modelCreate.gif){: .align_right}  

Clicking on an existing resource model or creating your own will bring up the Arches designer interface with the selected model's graph tree on the left (it will contain only a top node when first creating a new model). The Arches designer is separated into three sections (Graph, Cards, and Permissions) each of which manages a different aspect of designing resource models.
