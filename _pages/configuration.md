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
**Hexagon Size** changes the size of the hexagons that will appear on the map. Making your hexagons smaller will give a more detailed view of resource density while larger hexagons will provide a simpler and more general picture.
* **Hexagon Grid Precision** determines how precisely records are sorted into each bin. A higher integer will cause records to be sorted into the correct bin more frequently, but at a cost to performance.

**Warning:** A large project area combined with a small hexagon size and/or high precision will take a very long time to load, and can crash your browser. We suggest changing these settings in small increments to find the best combination for your project.
{: .notice--warning}

# Application settings
There are many settings in the settings_local.py and settings.py files that should be considered and set before further customizing the settings within Arches. Both the settings_local.py and settings.py can be found wherever you created your project under /[your  project name]/[your project name]. You can open these files in a code friendly text editor to make your changes. The settings_local.py file will override the settings.py file if there are any discrepancies in values between them. Most of the settings in settings.py are also in settings_local.py, so most of your changes should be made there while settings.py can be left mostly intact.

## Settings.py
Most of the settings in this file are also in settings_local.py and since it overwrites settings.py, it is optimal to do most of your configuring from settings_local.py to keep it all in one place. If you want to make changes in settings.py that also appears in settings_local.py, you will have to comment out the block where the setting appears or your change will be overwritten. Making your changes in settings_local.py also allows you to update settings.py without losing any changes you make.

### Security settings
The secret key used for production is stored here as 'SECRET_KEY' and you can toggle Django debugging on or off by changing the value of DEBUG

![Security Configuration]({{site.url}}/assets/images/securitySettings.PNG)

**Info:** Setting DEBUG to false will replace the more complex Django error messages with standard 404 and 500 error pages. It will also cause Django to stop serving static files, requiring you to set up an external webserver.
{: .notice--info}

## settings_local.py
A number of important database settings, formatting settings, cache settings, log settings, and account settings are configured from this file. Any changes made in settings_local.py will overwrite the values in settings.py.
### Time Formatting
- **Time wheel:** To configure you timewheel with custom bin sizes, follow this [guide to Time wheel configuration](https://arches.readthedocs.io/en/stable/additional-configuration/#time-wheel-configuration)
- **Time formats:** You can adjust the default time format for importing and exporting data by adjusting the value of 'DATE_IMPORT_EXPORT_FORMAT', which has the default '%Y-%m-%d' set initially.
^
### Dependencies and Database Management
- **Default file location:** The default location of user uploaded files is set through 'MEDIA_ROOT' and the max size of uploaded files is set through 'DATA_UPLOAD_MAX_MEMORY_SIZE'. For static files not uploaded by users, the default location is determined by 'STATIC_ROOT'.
- **Database settings:** Your default database is constructed under 'DATABASES', which requires differing parameters depending on which database backend you are using. You must define the engine and name the database, and some database backends will require additional user and host information.
![Database settings]({{site.url}}/assets/images/databaseSettigns.PNG)
- **Elasticsearch parameters:** Simple connection options and host settings for Elasticsearch can be set from here.
    - Changing the value of "timeout" will adjust how much latency will be tolerated before Elasticsearch times out a user
    - The values "host" and "port" allow you to set the name and address of your Elasticsearch instance for Arches to find and use
- **Installed apps:** Under 'INSTALLED_APPS' are the python paths to all external applications that are installed in your Django instance and provide auxiliary features.
- **Ontology Settings:** The name and location of the ontology to be used by your Reference Data Manager are set here. You can also add external packages to your Ontology by adding the names of the .xml files under 'ONTOLOGY_EXT'.
- **Coordinate system settings:** By changing the values under 'PREFERRED_COORDINATE_SYSTEMS' you can set a different coordinate system or adjust the projection, if your project calls for it. The coordinate system used by default is the WGS84, which  you can read more about [here](https://en.wikipedia.org/wiki/World_Geodetic_System).
^
### Email/Account Configuration
- **Default group:** Setting the value of 'USER_SIGNUP_GROUP' will adjust the default group that a newly created user is put into if another group is not specified.
- **Password settings:** Under 'AUTH_PASSWORD_VALIDATORS' are a number of different validators that control password requirements. You can add, remove, or adjust them to determine how strong of a password is required for users.
- **Email settings:** You can adjust 'EMAIL_HOST' and 'EMAIL_PORT' to control what Django uses for email correspondence when triggered by a custom function. 'EMAIL_HOST_USER' and 'EMAIL_HOST_PASSWORD' set the credentials for the SMTP server defined in 'EMAIL_HOST'. If left blank, Django will not attempt any authentication.
^
### Cache settings
-**Cache seeding:* To control how your cache is seeded, adjust 'CACHE_SEED_BOUNDS' and 'CACHE_SEED_MAX_ZOOM' to set the levels at which your cache seeds.
-**Tileserver settings:** You can set the location of your tileserver cache under 'TILE_CACHE_CONFIG'.
-**Timewheel Cache:** By adjusting 'CACHE_BY_USER' you can customize how often the Timewheel data is cached for specific users. You must first specify the usernames and then the duration (seconds) for which you want to cache the Timewheel. For example, it could look like 'CACHE_BY_USER = {'Resource Editor' : 3600}'
^
![Cache Settings]({{site.url}}/assets/images/cacheSettings.png)

### Log settings
-**Log preffernces:**
Under 'LOGGING' you can adjust 'format' to change the structure of the logs. The 'LEVEL:' fields control the verbosity of your terminal outputs, which can be set to four levels. From most to least verbose the options are: 'DEBUG', 'WARNING', 'ERROR', 'INFO'.
-**Log Location**
The write location for the standard logs can be set under 'LOGGING' by setting the 'filename' variable to a writable location. To set the location of the resource import log, change the value of 'RESOURCE_IMPORT_LOG' to the desired writable location.
^
![Log Configuration]({{site.url}}/assets/images/logSettings.PNG)
