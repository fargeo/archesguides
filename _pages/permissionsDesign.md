---
permalink: /admin-docs/permissions-design/
layout: single
title: Permissions
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
From the Permissions tab you can control the viewing and editing privileges of each user group. Permissions are set at the card level, so only the semantic nodes that form NodeGroups are selectable from the Permissions tab.
There are four permission privileges that can be set in different combinations for each user group and card:
- **Delete**: Allows users from the selected group to delete instances of the selected NodeGroup
- **No Access**: Prevents users from the selected group from viewing or editing the selected NodeGroup
- **Read**: Allows users from the selected group to view this NodeGroup on the map and on resource reports
- **Create/Update**: Allows users from the selected group to edit and create instances of the selected NodeGroup
