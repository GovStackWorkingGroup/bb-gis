---
description: This section lists the technical capabilities of this Building Block.
---

# 6 Functional Requirements

Section 4 of the GIS BB specification covers the key digital functionalities required for the management, processing, and use of geospatial information and their integration with other types of information and building blocks. The GIS BB offers these functionalities through RESTful API interfaces that exchange service requests and responses with external building blocks or applications. This section on functional requirements lists the technical components that each key digital function requires.

### 6.1 Map Display

##

## 6.1.1 Display Map (REQUIRED)

Provides access to and use of GIS data through a Data Viewer. A data Viewer may be a web-based, desktop, or mobile application that allows viewing and querying of GIS data. It can also be used for collaboration through note posting. Map Display views the graphic representation of geographic or spatial information related to the base map as well as business layers. Symbology (pre-defined styles) for each map layer will be displayed as a legend alongside the table of contents.

## 6.1.2 Manipulate Layers(REQUIRED)

Manipulates the Layer's Table of Contents on the GIS Data Viewer, which allows for manipulation of displayed data layers and access to such information as attributes, metadata, etc. Each map layer's symbology (pre-defined styles) will be displayed as a legend alongside the table of contents.

## 6.1.3 Spatial Bookmarks (RECOMMENDED)

Allows the user to capture the spatial extent of a given place or view of interest in the map display, give it a name, and be able to zoom to this exact extent whenever needed by selecting this name. Users can add, rename, and remove spatial bookmarks.

## 6.1.4 Find Coordinates (REQUIRED)

Allows the user to "Pan" to an existing X, Y location that the user enters.

## 6.1.4 Manage Map Settings (RECOMMENDED)

Allows users to set for each layer min & max scale limit for display purposes, whether or not a layer is identifiable and/or selectable. Settings are saved by the data viewer app as a cache and reserved for future data viewer displays. Settings are rest to default when the cache is cleared.

## 6.1.5 Take Notes (RECOMMENDED)

Allows the GIS user to add and share brief notes on the map display. Other users can view and comment on these notes. Notes can only be deleted by the creator of the note. Notes are saved and served as a web feature service (WFS).

## 6.7 Query GIS Data(REQUIRED)

provides transactions on and access to geographic features independently of the underlying data store.

## 6.8 Search Metadata (REQUIRED)

Retrieves metadata describing the layers and non-spatial tables offered by the GIS schema and their feature types from a data store.

## 6.9 Search Features and Attributes(REQUIRED)

Provides different options for retrieving features or values of feature properties embedded in GIS layers from the data store based on constraints, defined by the client, on feature properties.
