---
description: This section lists the technical capabilities of this Building Block.
---

# 6 Functional Requirements

Section 4 of the GIS BB specification covers the key digital functionalities required for managing, processing, and using geospatial information and their integration with other types of information and building blocks. The GIS BB offers these functionalities through RESTful API interfaces that exchange service requests and responses with external building blocks or applications. This section on functional requirements lists the technical components that each key digital function requires.

### 6.1 Map Display

* \[REQUIRED] The map display must provide access to GIS data through a data viewer (a web-based, desktop, or mobile application that allows viewing and querying of GIS data). The viewer should display a graphic representation (points, polygons, lines, or raster grids) of geographic or spatial information through thematic GIS layers or attribute tables. The symbology (pre-defined styles) for each map layer (how the geographic features of this layer are portrayed on the data viewer) must be displayed as a legend alongside a table of contents listing all layers provided by the service.
* \[REQUIRED] The map display must allow the data viewer to manipulate the displayed data layers. This includes hiding or displaying geographic features on the map display, changing their order, changing symbology, or classifying displayed geographic features. It must also provide access to attributes and metadata associated with the layer.
* \[REQUIRED] The map display must enable the GIS data viewer to offer the basic navigation capabilities of a typical GIS data viewer. This includes zooming in and out of a map, panning, searching for geographic features by attribute or by coordinates, and measuring distances and areas on the displayed map.
* \[RECOMMENDED] The map display should enable users to capture the spatial extent of a given location as a spatial bookmark in a GIS data viewer. Users should be able to name the bookmark and zoom to the exact extent whenever needed by selecting the bookmark's name. Users can also add, rename, and remove spatial bookmarks as necessary.
* \[RECOMMENDED] The map display should allow users to set minimum and maximum scale limits for each layer, specifying whether or not a layer is identifiable and/or selectable on the data viewer. These settings are saved as a cache by the data viewer app and are reserved for future data viewer displays. The settings are reset to default when the cache is cleared.
* \[OPTIONAL] The map display may allow the GIS user to add and share brief notes on the GID data viewer. Other users can view and comment on these notes. Notes can only be deleted by the creator of the note. Notes are saved and served as a web feature service.

### 6.2 GIS Query

* \[REQUIRED] The GIS query must allow for transactions on and access to geographic features independently of the underlying data store.
* \[REQUIRED] If feature metadata is not found in the metadata repository, the GIS Query must return a warning message.
* \[REQUIRED] The GIS query must retrieve metadata that describes the layers and non-spatial tables offered by the GIS schema and their feature types from a data store. The query results must display the title, abstract, author, keywords, data format, and a snippet of the queried layers, along with their spatial extent and temporal information. The service must provide the following options for the retrieved metadata:
  * Display the retrieved metadata record for all datasets and features meeting the selected criteria.
  * Generate and print metadata record reports for the datasets.
  * Visualize layers on a map view.
  * Download or import the layer to the data store (if the service permits).
* \[REQUIRED] The GIS query must allow searching for features and their attributes. It must also provide different options for retrieving features or values of feature properties embedded in GIS layers from the data store (e.g., selected features meeting the query criteria will be highlighted on the data viewer of the map display and the attributes table (as records corresponding to the selected features)). The query options should be based on constraints defined by the client, including:
  * Interactive selection of one or more features from the map display, either by directly clicking on them or using a graphical element (such as a box, circle, rectangle, transect, etc.).
  * Ad hoc SQL queries based on attribute tables.
  * Ad hoc queries based on locational information, such as geographic features located within a layer's boundaries, overlapping with a layer's boundaries, or near geographic features in a different layer.
  * Execution of a predefined query.

### 6.3 GIS Data Management

* \[REQUIRED] The GIS data management system must allow the publishing of the schema, metadata, and contents of a GIS datastore for data query, extraction, and retrieval by clients. To conform to standards, the vector contents of the GIS layers must be available as OGC Web Feature Service (WFS), while the raster contents must be available as OGC Web Coverage Service (WCS).
* \[REQUIRED] The GIS data management system must enable clients to retrieve geographic features and GIS layers (a collection of features) from the underlying data store based on simple selection criteria defined by the client.
* \[REQUIRED] The GIS data management system must present geometry-valued properties of geographic features in one of the supported Coordinate Reference Systems (CRS).
* \[REQUIRED] The GIS data management system must access and process the coordinates and geometry properties of geographic features and the bounding boxes of these features.
* \[REQUIRED] The GIS data management system must support editing operations of individual geographic features in GIS layers. Operations include:
  * adding or creating a new geographic feature in a GIS layer,
  * updating geographic features by either replacing them or modifying some of their properties,
  * deleting individual geographic features from a GIS layer.
* \[REQUIRED] The GIS data management system must support various replica operations for GIS features, layers, and databases, including creation, synchronization, and data extraction. It is up to the implementers of the service to decide how the GIS data management system will handle the creation of large replicas, synchronization of large numbers of edits, or extraction of large amounts of data.
* \[RECOMMENDED] The GIS data management system should provide the following access control levels for the editing capabilities provided by the services to control how the client can consume the services:
  * Editor permissions (at both the GIS layer and geographic feature levels) that control whether users can add, delete, or modify features in the service. For example, prevent or allow users from editing feature geometry.
  * Editor tracking that records who created or updated the features and when they did it. This is useful when accountability for the edits is required. An optional history tracking feature maintains information about feature changes over time, allowing edits to be rolled back.
  * Ownership-based access control that limits access to geographic features based on who created them.

### 6.4 Geocoding and Reverse Geocoding

* \[REQUIRED] The Geocoding and Reverse Geocoding service must provide a solid set of reference GIS layers (street parcels, street centerlines, postal codes, points of interest, landmarks, etc.), additional sets of potential aliases for these addresses, and a designated attribute table with designated fields that are used for geocoding, as well as indexes and local addressing knowledge that helps return the best match with an appropriate resolution.
* \[REQUIRED] The Geocoding and Reverse Geocoding service must provide the best match using explicit rules to promptly geocode locations (i.e., convert an address into geographic coordinates) or reverse geocode (convert geographic coordinates into an address) in an area of interest. Rules efficiency and performance depend on the underlying GIS data (e.g., land parcel vs. street centerline) and local knowledge.
* \[REQUIRED] The Geocoding and Reverse Geocoding service must be performed either from a single query (the address bar) or a batch query (e.g., a table file with multiple addresses or geographic coordinates).
* \[RECOMMENDED] The Geocoding and Reverse Geocoding service should offer multi-role and/or multiple reference data layers with different geometry types that can be combined and processed with the appropriate rules to interpret the geocoded location from many sources.
* \[RECOMMENDED] The Geocoding and Reverse Geocoding service should support multiple address formats if required by the implementation context.
* \[RECOMMENDED] The Geocoding and Reverse Geocoding service should support multiple languages if required by the implementation context.

### 6.5 Spatial Awareness and Analysis

### 6.6 Reporting

### 6.7 Geofencing

### 6.8 Routing
