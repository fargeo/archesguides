---
permalink: /admin-docs/groups-users/
layout: single
title: Groups and Users
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
Groups are a handy tool for organizing and managing your users. You can manage permissions for individual accounts, but in general it will be more efficient to group your users and set privileges based on these groups.

## Default Groups
Arches installs with a handful of pre-existing groups with permissions already set to help organize users. Groups are managed from the Django Administration page where all users and groups are created as well as edited.

**Tip:** It's best to leave the default groups that come with Arches intact and create your own new groups if you want to create different permission configurations.
{: .notice--info}

## Managing groups (Django admin)
**To create a new group for your project with custom permissions:**
1. Navigate to YourArchesHost/admin/
1. Under 'Authentication and Authorization' find the row labeled 'Groups' and click the ![Add]({{site.url}}/assets/images/djangoAdd.PNG) button on the right
1. Give the new group an appropriate name
1. Set the permissions you want users added to this group to have access to by selecting them under 'Available Permissions' and using the arrows to move them into 'Chose Permissions'
1. Click ![Save]({{site.url}}/assets/images/djangoSave.PNG) in the bottom right, you can now add users to this group  

![Editing group permissions in the Django interface]({{site.url}}/assets/GIFs/groupCreate.gif)

**To Edit an existing group:**
1. Navigate to YourArchesHost/admin/
1. Under 'Authentication and Authorization' find the row labeled 'Groups' and click the ![Change]({{site.url}}/assets/images/djangoChange.PNG) button on the right
1. Click on the name of the group you wish to edit
1. Edit the name of the group if you wish
1. Add any new permissions you want the group to have access to or remove any permissions you no longer want the group to have access too
1. Click ![Save]({{site.url}}/assets/images/djangoSave.PNG) in the bottom right to administer these changes to the group  

![Editing group permissions in the Django interface]({{site.url}}/assets/GIFs/groupEdit.gif)
