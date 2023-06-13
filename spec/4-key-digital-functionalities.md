---
description: >-
  Key digital functionalities describe the core (required) functions that this
  Building Block must be able to perform.
---

# 4 Key Digital Functionalities

The various actors and their activities described in section 2 must be supported by

### **4.1 Map Display**:&#x20;

The Map Display for GIS BB specifications is a fully configured GIS data viewing service that must:

* allow a set of configured information resources for GIS map display, navigation, layer manipulation, etc. to be passed between applications primarily, and support the distribution of search results.
* deliver georeferenced map images, vector features, and raster coverages in various supported formats.
* support a variety of geographic feature types (e.g., point, line, area).
* support a variety of map projections and map scales.
* allow users to explore geospatial data by panning, zooming, and rotating the map view. Users can also select and highlight specific data features to learn more about them.
* conform to all requirements of the following OGC standards: queryable Web Mapping Service (WMS), Web Feature Service (WFS), Web Map Tile Service (WMTS), Web Coverage Service (WCS), Web Processing Service (WPS), and Geopackage.

### **4.2 GIS Query**&#x20;

The GIS Query KDF for GIS BB specification enables the creation and execution of GIS data discovery and query operations.

* The discovery operations must allow the retrieval of GIS layer metadata and the definition of feature types (such as point, line, polygon, non-spatial table, etc.).
* The query operations must retrieve GIS features (layer's geometry information) or values (attributes attached to GIS features) interactively (_ad hoc_) or through predefined/stored query expressions. Queries can be made based on the attributes of a feature, its location, its geographic boundaries, or a mix of all three. Queries can be made with one or more attributes from the same or different GIS layers. They can also support spatiotemporal query operations if the underlying datastore supports spatiotemporal GIS (if the GIS attribute tables have timestamps or time-series capabilities).
* In addition, the GIS Query KDF must:
  * support standard SQL or spatial predicates (e.g., contains, overlaps, within, disjoint, touches, etc.).
  * enable the filtering of a query's results by specifying criteria such as location, attribute values, or time.
  * enable sorting a query's results by a specified field, such as name, value, or date.
  * allow viewing the query results in pages, which can be useful for large datasets.
  * allow to export the results of a query to various formats (e.g., CSV, KML, Shapefiles, etc.).
  * conform to and satisfy all requirements of the following OGC and ISO standards, including queryable Web Mapping Service (WMS), Web Feature Service (WFS), WFS Temporality Extension, Web Feature Service 2.0 Interface Standard, OGC API – Features, and ISO 19168-1:2020.

### 4.3 GIS Layer Management



### 4.4. Geocoding



### 4.5 Tabular Information Manipulation



### 4.6 Spatial Awareness and Analysis



### 4.7 Reporting



### 4.8 Geofencing&#x20;



### 4.9 Routing

4.10 Resource Tracking
