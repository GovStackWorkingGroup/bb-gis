---
description: >-
  Key digital functionalities describe the core (required) functions that this
  Building Block must be able to perform.
---

# 4 Key Digital Functionalities

The various actors and their activities described in Section 2 must be supported by the key digital functions, shown in the following diagram and detailed below.

<figure><img src=".gitbook/assets/image (2).png" alt=""><figcaption><p>Overview of the GIS BB KDFs</p></figcaption></figure>

### **4.1 Map Display**:

The Map Display for the GIS BB specifications is a fully configured GIS data viewing service that supports the passing of configured information resources between applications, delivers georeferenced map images and vector features in various formats, supports different geographic feature types, projections, and scales, allows users to explore data through panning, zooming, and rotating the map view, and conforms to OGC standards such as WMS, WFS, WMTS, WCS, WPS, and Geopackage.

### **4.2 GIS Query**

The GIS Query KDF enables the creation and execution of GIS data discovery and query operations. It allows retrieval of GIS layer metadata, definition of feature types, and retrieval of GIS features or values based on attributes, location, or boundaries. It supports standard SQL or spatial predicates, filtering and sorting of query results, viewing results in pages, and exporting results to various formats. It conforms to OGC and ISO standards.

### 4.3 GIS Data Management

The GIS Data Management KDF is a configurable service that allows users to access and perform various operations on a remote GIS database, including publishing metadata, querying data, replicating schemas, extracting and transferring data, manipulating tabular data, and synchronizing changes. It must conform to OGC standards such as CSW, WMS, WFS, WCS, and ISO 19107:2019 and ISO 19168-1:2020.

### 4.4. Geocoding and Reverse Geocoding

The Geocoding and Reverse Geocoding KDF for the GIS BB specifications convert addresses into coordinates and vice versa. It requires a large gazetteer of addresses and coordinates from various sources, can display coordinates on a map, and can find addresses for geographic features. It can also return results in different languages, filter searches, and conforms to the OGC Open Location Services Interface Standard.

### 4.5 Spatial Awareness and Analysis

The Spatial Awareness and Analysis KDF for GIS BB specification allows the design, authoring, and publishing of GIS analytical operations. It offers a range of processing operations and tools for geospatial awareness and analysis, including spatial analysis, data conversion, and map production. The KDF supports listing, describing, executing, and consuming GIS processes, as well as managing job status, cancellation, and result retrieval. It conforms to the OGC processing standards.

### 4.6 Reporting

The Reporting KDF for GIS BB specification outlines a framework for consistent reporting of GIS data. It includes the ability to select reporting templates, access GIS layers and attribute tables, specify a destination for reports, prioritize and schedule report delivery, manage the report queue, and adhere to OGC standards.

### 4.7 Geofencing

The Geofencing Key Delivery Framework (KDF) for GIS BB specification enables the creation and management of virtual geofences or redlines on a GIS map display. It allows users to draw, modify, and delete geofence boundaries, authorize and manage rules for geofences, track objects within geofences, and receive real-time alerts when objects enter or exit geofences. The framework also conforms to OGC API - Common and OGC API - Features standards.

### 4.8 Routing

The Routing KDF for GIS BB specification enables the creation and management of network routes independently of a specific routing engine. It computes new routes based on the shortest distance between starting and ending points and allows for the specification of additional routing rules and parameters. It also includes features such as service area parameters, route direction reports, and compliance with OGC standards.
