---
description: >-
  This section provides information on the core data structures/data models that
  are used by this Building Block.
---

# 7 Data Structures

The diagrams below illustrate the proposed resource models that demonstrate the connections between data objects that the GIS Building Block uses. The resource models are represented by a UML class diagram.  The GIS building block specification likely has many relationships between different resource types, such as layers, symbologies, and bookmarks. The class diagram concisely represents the structure and relationship between objects in the resource model.

## 7.1 Map Display

### 7.1.1 Map Display Resource Model

<figure><img src=".gitbook/assets/image (5).png" alt=""><figcaption><p><a href="https://drive.google.com/file/d/1EbdwOnPMpCHPEnjInAgOBco4TaYTh-xt/view?usp=sharing">Diagram Source</a></p></figcaption></figure>

### 7.1.2 Map Display: Data Elements

#### **7.1.2.1 MapDisplay**

<table><thead><tr><th width="162">Field</th><th width="205">Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>The title of the map display.</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>Description</td><td>String</td><td>A summary description of the map display, purpose and contents</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>Attribution</td><td>String</td><td>Information or credits displayed on the map</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>AccessControl </td><td>Boolean</td><td>Permissions or access restrictions for the map</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>EndPoint</td><td>String{url}</td><td>The URL or endpoint to access the API</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>CRS</td><td>String{coded_domain}</td><td>Code for the spatial reference system used by the map</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>Center_X</td><td>Real</td><td>The longitude coordinate of the center point of the map</td><td>Optional</td></tr><tr><td>Center_Y</td><td>Real</td><td>The latitude coordinate of the center point of the map</td><td>Optional</td></tr><tr><td>Bounds_MinX</td><td>Real</td><td>The longitude coordinate of the lower left point of the map bounding box</td><td></td></tr><tr><td>Bounds_MinY</td><td>Real</td><td>The latitude coordinate of the lower left point of the map bounding box</td><td></td></tr><tr><td>Bounds_MaxX</td><td>Real</td><td>The longitude coordinate of the upper right point of the map bounding box</td><td></td></tr><tr><td>Bounds_MaxY</td><td>Real</td><td>The latitude coordinate of the upper right point of the map bounding box</td><td></td></tr></tbody></table>

#### **7.1.2.2 Navigation**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Zoom</td><td>Boolean</td><td>Specifies if zooming is supported</td><td></td></tr><tr><td>ZoomLevel</td><td>Integer</td><td>The available zoom levels for the map</td><td>refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Pam</td><td>Boolean</td><td>Specifies if panning is supported</td><td></td></tr></tbody></table>

#### **7.1.2.3 SpatialBookmark**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Title or name given to the bookmark</td><td></td></tr><tr><td>Create</td><td>Integer</td><td>Specifies if creating bookmarks is supported.</td><td></td></tr><tr><td>Remove </td><td>Boolean</td><td>Specifies if renaming bookmarks is supported</td><td></td></tr><tr><td>Rename</td><td>Boolean</td><td>Specifies if removing bookmarks is supported</td><td></td></tr><tr><td>Zoom to</td><td>Boolean</td><td>Specifies if zooming to bookmark extents is supported</td><td></td></tr><tr><td>MinX</td><td>Real</td><td>The longitude coordinate of the lower left point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MinY</td><td>Real</td><td>The latitude coordinate of the lower left point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MaxX</td><td>Real</td><td>The longitude coordinate of the upper right point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MaxY</td><td>Real</td><td>The latitude coordinate of the upper right point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr></tbody></table>

#### **7.1.2.4 MapNote**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Creator</td><td>String</td><td>Name or identifier of the use who created the note</td><td></td></tr><tr><td>Content</td><td>String</td><td>The content of text of the map note</td><td></td></tr><tr><td>TimeSatmp</td><td>Date</td><td>The timestamp indicating when the note was create</td><td></td></tr><tr><td>Add</td><td>Boolean</td><td>Specifies if adding a map note is supported</td><td></td></tr><tr><td>Delete</td><td>Boolean</td><td>Specifies if deleting a map note is supported</td><td></td></tr><tr><td>View</td><td>Boolean</td><td>Specifies if viewing the content of a map note is supported</td><td></td></tr><tr><td>Visible</td><td>Boolean</td><td>Specifies if a map note is marketed on the map supported</td><td></td></tr><tr><td>X</td><td>Real</td><td>The longitude coordinate of the map note label on the map display</td><td>filled only when the visibility of the map note is True </td></tr><tr><td>Y</td><td>Real</td><td>The latitude coordinate of the map note label on the map display</td><td>filled only when the visibility of the map note is True </td></tr></tbody></table>

#### **7.1.2.5 Measuring**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Distance</td><td>Boolean</td><td>Specifies if measuring distances is supported</td><td></td></tr><tr><td>Area</td><td>Boolean</td><td>Specifies if measuring areas is supported</td><td></td></tr></tbody></table>

#### **7.1.2.6 LayerToC**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Visible</td><td>Boolean</td><td>Specifies if ToC is visible or hidden</td><td></td></tr><tr><td>LayerOrder</td><td>Array</td><td>Contains the layer IDs or names in the desired order, indicating how the layers should be displayed in the table of contents</td><td>The position of each layer in the array determines its placement in the table of contents, with the first element being the topmost layer and the last element being the bottommost layer</td></tr></tbody></table>

#### **7.1.2.7 Layer**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Title or name of the theme that the layer present</td><td></td></tr><tr><td>Description</td><td>String</td><td>A summary description of the layer, purpose and contents</td><td>refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Geometry</td><td>Object</td><td>An object representing the geometric shape and underlying coordinates and rules for point, line, polygon, curve GIS features,  or none.</td><td>If none, it is considered a non-spatial attribute table</td></tr><tr><td>Visible</td><td>Boolean</td><td>Specifies if the layer is visible or hidden on the map display </td><td></td></tr><tr><td>Selectable</td><td>Boolean</td><td>Specifies if the layer is selectable on the map display</td><td></td></tr><tr><td>Queryable</td><td>Boolean</td><td>Specifies if the layer can be queried</td><td></td></tr><tr><td>Editable</td><td>Boolean</td><td>Specifies if the layer is editable</td><td></td></tr><tr><td>Attribute 1</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with geographic features represented by the layer theme</td><td>The data type assigned will depend of the attribute type</td></tr><tr><td>.....................</td><td>.....................</td><td>.....................</td><td>.....................</td></tr><tr><td>Attribute n</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with geographic features represented by the layer theme</td><td>the data type assigned will depend on the attribute type</td></tr></tbody></table>

#### **7.1.2.8 ScaleLimit**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>MinScale</td><td>Integer</td><td>Specifies the minimum scale to dhow the layer's feature on map display</td><td>If set, the layer features disappear from the map display once zoom into beyond the minimum scale limit</td></tr><tr><td>MaxScale</td><td>Integer</td><td>Specifies the minimum scale to dhow the layer's feature on map display</td><td>If set, the layer features disappear from the map display once zoom out beyond the maximum scale limit</td></tr></tbody></table>

#### **7.1.2.9 Style**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>The name or identifier of the style applied to the layer</td><td>Styles define the symbology and map legends assigned to layers</td></tr><tr><td>Description</td><td>String</td><td>Text description of properties or parameters specific to the style</td><td>Refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Type</td><td>String (coded_domain)</td><td>A keyword or code to call a predefined style of version in defined or served by OGC API Styles</td><td>Style codes or identifiers can be fetched through GC API Styles Part I - check <a href="https://developer.ogc.org/api/styles/index.html">https://developer.ogc.org/api/styles/index.html</a></td></tr></tbody></table>

#### **7.1.2.10 DataViewer**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Type</td><td>String (coded_domain)</td><td>A domain code specifying whether the client data viewer is desktop, mobile, web browser, or unknown.</td><td>The type of client accessing GIS APIs, may have some implications in terms of interactivity and user experience (navigation, layer manipulation, etc.)</td></tr></tbody></table>

## 7.2 GIS Query

## 7.3 GIS Data Management

## 7.4 Geocoding and Reverse Geocoding

## 7.5 Spatial Awareness and Analysis&#x20;

## 7.6 Reporting

## 7.7 Geofencing

## 7.8 Routing
