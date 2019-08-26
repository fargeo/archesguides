---
permalink: /admin-docs/card-design/
layout: single
title: Cards
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
User interface is controlled from the cards tab. The node structure of your resource model will be shown by the card tree on the left. Each NodeGroup defined by a semantic node makes up one card. Each node in a NodeGroup is controlled by a widget on that NodeGroups card. You can click on a semantic node to view the card for its NodeGroup, or click on a node to jump to its card and select its widget.

Selecting a semantic node will bring up the card configuration for that NodeGroups card. From there you can click on any of that cards widgets to view the widget manager (you can click on a widget directly or click on a node in the card tree to bring up the widget manager for that node).
![Editing card design]({{site.url}}/assets/GIFs/cardManager.gif)

Card configuration gives you control over how users will see and interact with a card. You can adjust the labeling, styling, and data structure of a card from here. The widget manager allows you to decide how the data for each specific node will be entered and stored. Depending on a Node's datatype, you will have different widget options along with display and data structure settings.

**Tip:**
You can open the help built into Arches while on the card tab for a description of every individual Card Configuration and Widget Management setting.
{: .notice--info}
