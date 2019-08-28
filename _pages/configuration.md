---
permalink: /admin-docs/configuration/
layout: single
title: System Settings
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
System settings within Arches are stored in a special settings resource model that is part of your project's database. Settings are displayed in a card tree and are adjusted in a similar fashion to typical records. You can select any card to make changes and then select "save edit" to implement these settings adjustments.
# Map settings

Under 'Default Map Settings' you can:
* Set your MapBox API key (you will need to enter one of these for the Arches map to function).
* Change the geographical area of your project, which determines the bounds of the search function and the extent your hexagon bins will cover.

**Info:** Upon navigating to the search page, the map will automatically zoom to your project extent that you set here.
{: .notice--info}
* Set the default, maximum, and minimum zoom values to control the initial zoom level as well as the amount users are allowed to zoom in or out. These should be three integers between zero and twenty with  Min Zoom <= Default Zoom <= Max Zoom.

# Hexbin
Arches can group search results and display them as hexagonal bins using an overlay, but you have to do some configuring ahead of time for it to be effective for your project. There are two key hexbin settings located with the other default map settings under 'Search Results Grid':
* **Hexagon Size** changes the size of the hexagons that will appear on the map. Making your hexagons smaller will give a more detailed view of resource density while larger hexagons will provide a simpler and more general picture.
* **Hexagon Grid Precision** determines how precisely records are sorted into each bin. A higher integer will cause records to be sorted into the correct bin more frequently, but at a cost to performance.

**Warning:** A large project area combined with a small hexagon size and/or high precision will take a very long time to load, and can crash your browser. We suggest changing these settings in small increments to find the best combination for your project.
{: .notice--warning}

# Application settings
There are many settings in the settings_local.py and settings.py files that should be considered and set before further customizing the settings within Arches. Both the settings_local.py and settings.py can be found wherever you created your project under /[your  project name]/[your project name]. You can open these files in python Idle or other code friendly text editor to make your changes.

## Settings.py
A number of important user settings, security settings, and directory settings are configured from this file. Most of these settings are applied through Django.
### Upload settings
You can set the destination directory for uploaded files by changing the value of MEDIA_ROOT
### Log settings
Settings for both the regular and import logs are managed within settings.py. You can set the directory where the logs are kept and change the format of the log entries, along with other optional adjustments.
The 'LEVEL:' fields control the verbosity of your terminal outputs, which can be set to four levels. From most to least verbose the options are: 'DEBUG', 'WARNING', 'ERROR', 'INFO'.

![Log Configuration]({{site.url}}/assets/images/loggingConfigurationAnnotated.png)
### Security settings
The secret key used for production is stored here as SECRET_KEY and you can toggle django debugging on or off by changing the value of DEBUG


![Security Configuration]({{site.url}}/assets/images/securitySettingsAnnotated.png)

**Info:** Setting DEBUG to false will replace the more complex Django error messages with standard 404 and 500 error pages. It will also cause Django to stop serving static files, requiring you to set up an external webserver.
{: .notice--info}
### Host settings/permissions
You can change the database host and set other host permissions as well as adjusting other PostGIS settings that were given their initial value during your installation of Arches.


![Host Configuration]({{site.url}}/assets/images/hostSettingsAnnotated.png)
### Cache settings
Near the bottom of your settings.py, you can set the location for your Tile and Django caches along with some other configurable attributes. To control how your cache is seeded, adjust 'CACHE_SEED_BOUNDS' and 'CACHE_SEED_MAX_ZOOM' to set the levels at which your cache seeds. You can also set the location of your tileserver cache under 'TILE_CACHE_CONFIG'.

![Host Configuration]({{site.url}}/assets/images/cacheSettings.png)

## settings_local.py
This file contains some basic options for data presentation and access as well as a few user account settings. The settings_local.py file will override the settings.py file if there are any discrepancies in values between them.
### Time Formatting
- **Time wheel**
To configure you timewheel with custom bin sizes, follow this [guide to Time wheel configuration](https://arches.readthedocs.io/en/stable/additional-configuration/#time-wheel-configuration)
- **Time formats**
You can adjust the default time format for importing and exporting data, which is '%Y-%m-%d'
^
### Dependencies and Database Management
- **Default file location**
The default location of user uploaded files is set through 'MEDIA_ROOT' and the max size of uploaded files is set through 'DATA_UPLOAD_MAX_MEMORY_SIZE'. For static files not uploaded by users, the default location is determined by 'STATIC_ROOT'.
- **Database settings**
Your default database is constructed under 'DATABASES', which requires differing parameters depending on which database backend you are using. You must define the engine and name the database, and some database backends will require additional user and host information.
- **Elasticsearch parameters**
Simple connection options and host settings for Elasticsearch can be set from here.
    - Changing the value of "timeout" will adjust how much latency will be tolerated before Elasticsearch times out a user
    - The values "host" and "port" allow you to set the name and address of your Elasticsearch instance for Arches to find and use
- **Installed apps**
Under 'INSTALLED_APPS' are the python paths to all external applications that are installed in your Django instance and provide auxiliary features.
- **Ontology Settings**
The name and location of the ontology to be used by your Reference Data Manager are set here. You can also add external packages to your Ontology by adding the names of the .xml files under 'ONTOLOGY_EXT'.
^
### Email/Account Configuration
- **Default group**
Setting the value of 'USER_SIGNUP_GROUP' will adjust the default group that a newly created user is put into if another group is not specified.
- **Password settings**
Under 'AUTH_PASSWORD_VALIDATORS' are a number of different validators that control password requirements. You can add, remove, or adjust them to determine how strong of a password is required for users.
- **Email settings**
You can adjust 'EMAIL_HOST' and 'EMAIL_PORT' to control what Django uses for email correspondence when triggered by a custom function. 'EMAIL_HOST_USER' and 'EMAIL_HOST_PASSWORD' set the credentials for the SMTP server defined in 'EMAIL_HOST'. If left blank, Django will not attempt any authentication.
^
