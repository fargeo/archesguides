---
permalink: /admin-docs/app-settings/
layout: single
title: Application Settings
sidebar:
  nav: "admin docs"
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
You can customize the application settings of your project to create an ideal environment for your users. There are some basic system data and search settings that can be configured for your project's users in the System Settings tab of the Arches UI.
**From System Data Settings you can:**
- Change the default application name, which is displayed in the browser title bar and identifies the application in other locations
- Enter a key for Google web analytics if you plan to track the traffic to your Arches Application
- Add Thesaurus SPARQL Endpoints, which will appear in the RDM and allow you to import different Thesauri from the external source specified in the endpoint
^
**From System Settings the search settings you can change are:**
- Number of search results per page, which dictates how many results will be shown per page in the list on the left as well as how many markers will be placed on the map at one time
- Number of search hints per dropdown, which determines how many suggested queries are displayed below the search bar when a user is typing a search
- Max number of search results to export, which sets the limit for how many results of a query can be exported to a .csv or .shp
- Saved searches, which allows you to save a set of filters and give them a name. This search will then be available to your users on the main search tab under ![Saved searches tab]({{site.url}}/assets/images/savedSearch.PNG) so your query and results can be replicated
^
