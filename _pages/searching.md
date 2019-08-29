---
permalink: /user-docs/searching/
layout: single
title: Searching Arches
sidebar:
  nav: "user docs"
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
The search tab in Arches is used to find and select resource models from your project. Search results are displayed in list form to the left and on the map to the right.  

![Search Results]({{site.url}}/assets/images/searchResultsAnnotated.png)
# Filtering
There are multiple parameters you can choose to filter your search results by. Multiple filters can be layered together to further narrow your results and all of the currently applied filters will be displayed in the search field. These filters can be inverted to exclude the queried field by clicking the colored box or removed independently by clicking the 'x' inside each filters colored box.  

![Search Filtering]({{site.url}}/assets/images/searchFilteringAnnotated.png)
## By concept
Searching by concept functions like a typical search bar for all of the concepts in your projects Thesauri. As you type Arches will suggest possible concepts or resources that contain whatever text you have entered.  

![Search by Concept]({{site.url}}/assets/GIFs/searchByConcept.gif)
## By area
Searching by area allows you to sort results based on their geographical location. You can create an area around a point, line, or polygon.

To create an area filter:
1. Select one of the draw options from the menu bar on the left side of the Map and set the buffer distance from the boundary in which you want results to be included ![Area menu]({{site.url}}/assets/images/areaMenu.PNG){: .align-right}
  
2. Click anywhere on the map to create your first point (markers only have one point)
3. If you're drawing a polyline or polygon, click elsewhere on the map to create more connecting points and Arches will show your shape as you construct it
4. Once you finished adding points, hit 'Enter' to finish the shape and your results will be filtered to only what falls within your drawing
5. If you drew a polyline or polygon, click on your shape to display the buffer zone and include the resources within it in your results

![Search by Area Line]({{site.url}}/assets/GIFs/searchByLine.gif)
## By time
Time filters require you to select the type of time range you want to sort by from the appropriate resource model you're searching for. You can either enter a range in the time filter or select one from the time wheel.  

![Search by Time Filter]({{site.url}}/assets/GIFs/searchByTimeFilter.gif)  

![Search by Time Wheel]({{site.url}}/assets/GIFs/searchByWheel.gif)
## Advanced Search
Advanced search gives you the power to select any data field from a particular resource model and filter your results through it. These advanced filters allow for more precise searching and can be layered similarly to regular filters.
# Viewing Results
Below the search bar Arches will display how many results your query yielded and below that the results will be shown on in list form. All of the results that show up on the first page of the list will also have a marker placed on the map.
## Selecting resources
You can open a resource to view or edit it from the list view on the left or from the map on the right. Click on any map marker to bring up a window with options for that resource. To open the resource report, click the title of the record in the list or the ![report button]({{site.url}}/assets/images/reportButton.PNG) button on the resource window brought up on the map. To open the resource in the resource editor, click the ![Edit button]({{site.url}}/assets/images/editButton.png) on the resources entry in the list or on the resource window if using the map.
