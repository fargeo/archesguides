---
permalink: /admin-docs/configuration/
layout: single
title: System Configuration
sidebar:
  nav: "admin docs"
toc: true
toc_label: "Table of Contents"
toc_icon: "file-alt"
toc_sticky: true
defaults:
  # _pages
  - scope:
      type: pages
    values:
      author_profile: false
---
# System settings
System settings within Arches are stored in a special settings resource model that is part of your project's database. Settings are displayed in a card tree and are adjusted in a similar fashion to typical records. You can select any card to make changes and then select "save edit" to implement these settings adjustments.
## Map settings
Under 'Default Map Settings' you can:
* Set your MapBox API key (you will need to enter one of these for the Arches map to function).
* Change the geographical area of your project, which determines the bounds of the search function and the extent your hexagon bins will cover.

**Info:** Upon navigating to the search page, the map will automatically zoom to your project extent that you set here.
{: .notice--info}
* Set the default, maximum, and minimum zoom values to control the initial zoom level as well as the amount users are allowed to zoom in or out. These should be three integers between zero and twenty with  Min Zoom <= Default Zoom <= Max Zoom.
## Hexbin
Arches can group search results and display them as hexagonal bins using an overlay, but you have to do some configuring ahead of time for it to be effective for your project. There are two key hexbin settings located with the other default map settings under 'Search Results Grid':
* **Hexagon Size** changes the size of the hexagons that will appear on the map. Making your hexagons smaller will give a more detailed view of resource density while larger hexagons will provide a simpler and more general picture.
* **Hexagon Grid Precision** determines how precisely records are sorted into each bin. A higher integer will cause records to be sorted into the correct bin more frequently, but at a cost to performance.

**Warning:** A large project area combined with a small hexagon size and/or high precision will take a very long time to load, and can crash your browser. We suggest changing these settings in small increments to find the best combination for your project.
{: .notice--warning}

# Application settings
There are many settings in the settings_local.py and settings.py files that should be considered and set before further customizing the settings within Arches. Both the settings_local.py and settings.py can be found wherever you created your project under /[your  project name]/[your project name]. You can open these files in python Idle or other code friendly text editor to make your changes.
## Settings_local.py
This file contains some basic options for data presentation and access as well as a few user account settings.
### Time wheel
### Default file location
### Database settings
### Elasticsearch parameters
### Time formats
### Default group
### Password settings
### Email settings
### Installed apps
### Ontology Settings

## Settings.py
A number of important user settings, security settings, and directory settings are configured from this file. Most of these settings work through django.
### Upload settings
You can set the destination directory for uploaded files by changing the value of MEDIA_ROOT
### Log settings
Settings for both the regular and import logs are managed within settings.py. You can set the directory where the logs are kept and change the format of the log entries, along with other optional adjustments.


![Log Configuration]({{site.url}}/assets/images/loggingConfigurationAnnotated.png){: .full}
### Security settings
The secret key used for production is stored here as SECRET_KEY and you can toggle django debugging on or off by changing the value of DEBUG


![Security Configuration]({{site.url}}/assets/images/securitySettingsAnnotated.png){: .full}

**Info** Setting DEBUG to false will replace the more complex Django error messages with standard 404 and 500 error pages. It will also cause Django to stop serving static files, requiring you to set up an external webserver.
{: .notice--info}
### Host settings/permissions
You can change the database host and set other host permissions as well as adjusting other PostGIS settings that were given their initial value during your installation of Arches.


![Host Configuration]({{site.url}}/assets/images/hostSettingsAnnotated.png){: .full}
### Cache settings
Near the bottom of your settings.py, you can set the location for your Tile and Django caches along with some other configurable attributes.  

    
![Host Configuration]({{site.url}}/assets/images/cacheSettings.png){: .full}
