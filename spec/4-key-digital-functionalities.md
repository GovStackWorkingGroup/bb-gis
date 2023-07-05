---
description: >-
  Key digital functionalities describe the core (required) functions that this
  Building Block must be able to perform.
---

# 4 Key Digital Functionalities

The various actors and their activities described in Section 2 must be supported by the key digital functions, shown in the following diagram and detailed below.&#x20;

<div align="center">

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

</div>

### **4.1 Map Display**:

The Map Display for the GIS BB specifications is a fully configured GIS data viewing service that must:

* allow a set of configured information resources for GIS map display, navigation, layer manipulation, etc. to be passed between applications primarily, and support the distribution of search results.
* deliver georeferenced map images, vector features, and raster coverages in various supported formats.
* support a variety of geographic feature types (e.g., point, line, area).
* support a variety of map projections and map scales.
* allow users to explore geospatial data by panning, zooming, and rotating the map view. Users can also select and highlight specific data features to learn more about them.
* conform to all requirements of the following OGC standards: queryable Web Mapping Service (WMS), Web Feature Service (WFS), Web Map Tile Service (WMTS), Web Coverage Service (WCS), Web Processing Service (WPS), and Geopackage.

### **4.2 GIS Query**&#x20;

The GIS Query KDF for the GIS BB specification enables the creation and execution of GIS data discovery and query operations.

* The discovery operations must allow the retrieval of GIS layer metadata and the definition of feature types (such as point, line, polygon, non-spatial table, etc.).
* The query operations must retrieve GIS features (layer's geometry information) or values (attributes attached to GIS features) interactively (_ad hoc_) or through predefined/stored query expressions. Queries can be made based on the attributes of a feature, its location, its geographic boundaries, or a mix of all three. Queries can be made with one or more attributes from the same or different GIS layers. They can also support spatiotemporal query operations if the underlying datastore supports spatiotemporal GIS (if the GIS attribute tables have timestamps or time-series capabilities).
* In addition, the GIS Query KDF must:
  * support standard SQL or spatial predicates (e.g., contains, overlaps, within, disjoint, touches, etc.).
  * enable the filtering of a query's results by specifying criteria such as location, attribute values, or time.
  * enable sorting a query's results by a specified field, such as name, value, or date.
  * allow viewing the query results in pages, which can be useful for large datasets.
  * allow to export the results of a query to various formats (e.g., CSV, KML, Shapefiles, etc.).
  * conform to and satisfy all requirements of the following OGC and ISO standards, including OGC catalogue service for the web (CSW), queryable Web Mapping Service (WMS), Web Feature Service (WFS), WFS Temporality Extension, Web Feature Service 2.0 Interface Standard, and ISO 19168-1:2020.

### 4.3 GIS Layer Management

The GIS Data Management KDF for the GIS BB specifications is a configurable service that allows system and user actors to access data and features of a remote database and perform one or more of the following operations:

* Publish metadata descriptions of a GIS database schema and its layer and table contents.
* Query GIS data (layers and tables) of a remote GIS database.
* Replicate a remote GIS database schema.
* Extract and transfer GIS data layers or features from a remote GIS database.
* Create, edit, modify, or delete geographic features on the extracted GIS data layers.
* Tabular data manipulation.
* Synchronize changes in several distributed databases over the Internet.

The GIS Data Management KDF must conform to and satisfy all requirements of the following OGC standards, including OGC Catalogue Service for the Web (CSW), Queryable Web Mapping Service (WMS), Web Feature Service (WFS), Web Coverage Service (WCS), and ISO 19107:2019 and ISO 19168-1:2020 standards.

### 4.4. Geocoding and Reverse Geocoding&#x20;

The Geocoding and Reverse Geocoding KDF for the GIS BB specifications convert human-readable addresses into geographic coordinates and vice versa. Geocoding involves converting an address into latitude and longitude coordinates, while reverse geocoding involves converting latitude and longitude coordinates into an address. This KDF must:

* be powered by a large gazetteer of addresses and geographic coordinates compiled from various sources, such as government records, commercial databases, and user-submitted data.
* find the latitude and longitude coordinates of a given address or geographical place and display it as a map display feature.
* find an address or a place for a given geographic feature and display it as a label on a map display.
* return candidate addresses or places in different languages and locales.
* Refine and filter the search by various criteria such as category, feature type, etc.
* conform to and satisfy all requirements of the OGC Open Location Services Interface Standard (OpenLS).

### 4.5 Spatial Awareness and Analysis

The Spatial Awareness and Analysis KDF for GIS BB specification enables the design, authoring, and publishing of GIS analytical operations that system and user actors can consume. These operations can perform various tasks, such as spatial analysis, data conversion, and map production. This KDF must:

* allow listing all supposed GIS processing operations and tools it offers for geospatial awareness and analysis.
* return a detailed description of the process.
* execute a process.
* allow a process to consume GIS data.
* list the running and finished jobs.
* return the status of a job.
* cancel a job execution.
* return the result of a job.
* conform to and satisfy all requirements of the OGC processing standards.

### 4.6 Reporting

The Reporting KDF for GIS BB specification provides a generic framework for consistently reporting GIS data, including defining the type and format of the generated report according to pre-defined reporting templates and the delivery of the reports. This KDF must:

* allow selection among these types of reporting templates: map-based, chart-based, statistical-based, event-based, and resource-based.
* allow access to GIS layers and attribute tables in a GIS database or data store.
* allow for the specification of a destination point to which the report will be sent.
* allow for the prioritization and scheduled delivery of reports.
* allow for the management of the report queue, including recalling reports.
* conform to and satisfy all requirements of applicable OGC standards, including the OGC API for Styles and the OGC API for Records.

### 4.7 Geofencing&#x20;

The Geofencing Key Delivery Framework (KDF) for GIS BB specification allows for the creation and management of virtual "geofences" or "redlines" on a GIS map display. Geofences or redlines are polygonal areas or sketches drawn on a GIS map display and used to track objects that cross the virtual boundaries of the sketch using devices such as mobile phones, GPS trackers, and RFID tags. This KFD must:

* allow the user to draw, create, modify, or delete geofence boundaries on the GIS map display.
* authorize and manage rules for the geofence boundaries and track the objects within the geofence (e.g., designate which objects need to be tracked, setting "entry" and "exit" events, etc.).
* create, send, and receive alerts when tracked objects enter or exit geofences in real time.
* designate users or systems to receive geofencing alerts.
* conform with the OGC API - Common and the OGC API - Features standards.

### 4.8 Routing

The Routing KDF for GIS BB specification allows human or system actors to generate and manage network routes based on an underlying GIS road network. This KFD must:

* enable the creation and management of routes independently of a specific routing engine or algorithm.
* compute new routes based on a starting and ending point using the shortest distance.
* specify additional routing rules and parameters (e.g., type of route (cars, buses, human), route barriers such as traffic conditions or the presence of over- and under-passes, adding stopping points, traffic conditions, road-turn directions, etc.).
* create and manage service area parameters along the route (e.g., all gas stations within 2 KM of the route).
* create route direction reports such as directions, turns, or time and distance charts for multiple locations along the route, etc.,&#x20;
* conform to and satisfy all requirements of applicable OGC standards, including OGC API for Routes.
