---
description: >-
  This section provides information on the core data structures/data models that
  are used by this Building Block.
---

# 7 Data Structures

The diagram below illustrates the proposed resource model that demonstrates the connections between data objects that the GIS Building Block uses. The resource models are represented by a UML class diagram.  The GIS building block specification likely has many relationships between different resource types, such as layers, symbologies, and bookmarks. The class diagram concisely represents the structure and relationship between objects in the resource model.

## 7.1 Resource Model

<figure><img src=".gitbook/assets/Govstack_GIS_BB_Resource_Model.drawio (4).png" alt=""><figcaption><p><a href="https://app.diagrams.net/#G19wpPBMka6gAqAPfduKZ_fDAwffVpV9f5">Diagram Source</a></p></figcaption></figure>

## 7.2 Data Elements

### 7.2.1 Group: Map Display

#### &#x20;**MapDisplay**

<table><thead><tr><th width="162">Field</th><th width="205">Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>The title of the map display.</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>Description</td><td>String</td><td>A summary description of the map display, purpose and contents</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>Attribution</td><td>String</td><td>Information or credits displayed on the map</td><td>refer to OGC API Common <a href="https://ogcapi.ogc.org/common/">https://ogcapi.ogc.org/common/</a></td></tr><tr><td>AccessControl </td><td>Boolean</td><td>Permissions or access restrictions for the map</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>EndPoint</td><td>String{url}</td><td>The URL or endpoint to access the API</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>CRS</td><td>String{coded_domain}</td><td>Code for the spatial reference system used by the map</td><td>refer to OGC API Map Part II:  <a href="https://docs.ogc.org/is/18-058/18-058.html">https://docs.ogc.org/is/18-058/18-058.html</a></td></tr><tr><td>Center_X</td><td>Real</td><td>The longitude coordinate of the center point of the map</td><td>Optional</td></tr><tr><td>Center_Y</td><td>Real</td><td>The latitude coordinate of the center point of the map</td><td>Optional</td></tr><tr><td>Bounds_MinX</td><td>Real</td><td>The longitude coordinate of the lower left point of the map bounding box</td><td></td></tr><tr><td>Bounds_MinY</td><td>Real</td><td>The latitude coordinate of the lower left point of the map bounding box</td><td></td></tr><tr><td>Bounds_MaxX</td><td>Real</td><td>The longitude coordinate of the upper right point of the map bounding box</td><td></td></tr><tr><td>Bounds_MaxY</td><td>Real</td><td>The latitude coordinate of the upper right point of the map bounding box</td><td></td></tr></tbody></table>

#### **Navigation**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Zoom</td><td>Boolean</td><td>Specifies if zooming is supported</td><td></td></tr><tr><td>ZoomLevel</td><td>Integer</td><td>The available zoom levels for the map</td><td>refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Pan</td><td>Boolean</td><td>Specifies if panning is supported</td><td></td></tr></tbody></table>

#### **SpatialBookmark**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Title or name given to the bookmark</td><td></td></tr><tr><td>Create</td><td>Integer</td><td>Specifies if creating bookmarks is supported.</td><td></td></tr><tr><td>Remove </td><td>Boolean</td><td>Specifies if removing bookmarks is supported</td><td></td></tr><tr><td>Rename</td><td>Boolean</td><td>Specifies if renaming bookmarks is supported</td><td></td></tr><tr><td>Zoom to</td><td>Boolean</td><td>Specifies if zooming to bookmark extents is supported</td><td></td></tr><tr><td>MinX</td><td>Real</td><td>The longitude coordinate of the lower left point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MinY</td><td>Real</td><td>The latitude coordinate of the lower left point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MaxX</td><td>Real</td><td>The longitude coordinate of the upper right point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr><tr><td>MaxY</td><td>Real</td><td>The latitude coordinate of the upper right point of the spatial extent captured by the bookmark </td><td>filled only when the spatial bookmark "Create" is  True </td></tr></tbody></table>

#### **MapNote**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Creator</td><td>String</td><td>Name or identifier of the use who created the note</td><td></td></tr><tr><td>Content</td><td>String</td><td>The content of text of the map note</td><td></td></tr><tr><td>TimeSatmp</td><td>Date</td><td>The timestamp indicating when the note was create</td><td></td></tr><tr><td>Add</td><td>Boolean</td><td>Specifies if adding a map note is supported</td><td></td></tr><tr><td>Delete</td><td>Boolean</td><td>Specifies if deleting a map note is supported</td><td></td></tr><tr><td>View</td><td>Boolean</td><td>Specifies if viewing the content of a map note is supported</td><td></td></tr><tr><td>Visible</td><td>Boolean</td><td>Specifies if marking a map note on the map supported</td><td></td></tr><tr><td>X</td><td>Real</td><td>The longitude coordinate of the map note label on the map display</td><td>filled only when the visibility of the map note is True </td></tr><tr><td>Y</td><td>Real</td><td>The latitude coordinate of the map note label on the map display</td><td>filled only when the visibility of the map note is True </td></tr></tbody></table>

#### **Measuring**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Distance</td><td>Boolean</td><td>Specifies if measuring distances is supported</td><td></td></tr><tr><td>Area</td><td>Boolean</td><td>Specifies if measuring areas is supported</td><td></td></tr></tbody></table>

#### **LayerToC**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Visible</td><td>Boolean</td><td>Specifies if ToC is visible or hidden</td><td></td></tr><tr><td>LayerOrder</td><td>Array</td><td>Contains the layer IDs or names in the desired order, indicating how the layers should be displayed in the table of contents</td><td>The position of each layer in the array determines its placement in the table of contents, with the first element being the topmost layer and the last element being the bottommost layer</td></tr></tbody></table>

#### **Layer**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Title or name of the theme that the layer presents</td><td></td></tr><tr><td>Description</td><td>String</td><td>A summary description of the layer, purpose and contents</td><td>refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Geometry</td><td>Object</td><td>An object representing the geometric shape and underlying coordinates and rules for point, line, polygon, curve GIS features,  or none.</td><td>If none, it is considered a non-spatial attribute table</td></tr><tr><td>Visible</td><td>Boolean</td><td>Specifies if the layer is visible or hidden on the map display </td><td></td></tr><tr><td>Selectable</td><td>Boolean</td><td>Specifies if the layer is selectable on the map display</td><td></td></tr><tr><td>Queryable</td><td>Boolean</td><td>Specifies if the layer can be queried</td><td></td></tr><tr><td>Editable</td><td>Boolean</td><td>Specifies if the layer is editable</td><td></td></tr><tr><td>Attribute 1</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with geographic features represented by the layer theme</td><td>The data type assigned will depend of the attribute type</td></tr><tr><td>.....................</td><td>.....................</td><td>.....................</td><td>.....................</td></tr><tr><td>Attribute n</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with geographic features represented by the layer theme</td><td>the data type assigned will depend on the attribute type</td></tr></tbody></table>

#### **NonSpatialTable**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Title or name of the theme that the table presents</td><td></td></tr><tr><td>Description</td><td>String</td><td>A summary description of the Table, purpose and contents</td><td>refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Queryable</td><td>Boolean</td><td>Specifies if the table can be queried</td><td></td></tr><tr><td>Editable</td><td>Boolean</td><td>Specifies if the table is editable</td><td></td></tr><tr><td>Attribute 1</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with records represented by the layer theme</td><td>The data type assigned will depend of the attribute type</td></tr><tr><td>.....................</td><td>.....................</td><td>.....................</td><td>.....................</td></tr><tr><td>Attribute n</td><td>"variable"</td><td>Represents a descriptive information or characteristic associated with the records represented by the layer theme</td><td>the data type assigned will depend on the attribute type</td></tr></tbody></table>

#### **ScaleLimit**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>MinScale</td><td>Integer</td><td>Specifies the minimum scale to show the layer's feature on map display</td><td>If set, the layer features disappear from the map display once zoom into beyond the minimum scale limit</td></tr><tr><td>MaxScale</td><td>Integer</td><td>Specifies the minimum scale to show the layer's feature on map display</td><td>If set, the layer features disappear from the map display once zoom out beyond the maximum scale limit</td></tr></tbody></table>

#### **Style**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>The name or identifier of the style applied to the layer</td><td>Styles define the symbology and map legends assigned to layers</td></tr><tr><td>Description</td><td>String</td><td>Text description of properties or parameters specific to the style</td><td>Refer to OGC API Map Part I: <a href="https://docs.ogc.org/is/20-057/20-057.html">https://docs.ogc.org/is/20-057/20-057.html</a></td></tr><tr><td>Type</td><td>String (coded_domain)</td><td>A keyword or code to call a predefined style of version in defined or served by OGC API Styles</td><td>Style codes or identifiers can be fetched through GC API Styles Part I - check <a href="https://developer.ogc.org/api/styles/index.html">https://developer.ogc.org/api/styles/index.html</a></td></tr></tbody></table>

#### **DataViewer**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Type</td><td>String (coded_domain)</td><td>A domain code specifying whether the client data viewer is desktop, mobile, web browser, or unknown.</td><td>The type of client accessing GIS APIs, may have some implications in terms of interactivity and user experience (navigation, layer manipulation, etc.)</td></tr></tbody></table>

#### **LayerMetadata**&#x20;

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Title of the dataset or feature</td><td></td></tr><tr><td>Abstract</td><td>String</td><td>Abstract description of the dataset or feature</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Author</td><td>String</td><td>Author description</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Geometry</td><td>String {coded_domain}</td><td>Codes representing the geometry type of the layer (point, line, polygon, non-spatial)</td><td></td></tr><tr><td>Keywords</td><td>String</td><td>Keywords associated with the dataset or feature</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Snippet</td><td>Object</td><td>Snippet or summary of the dataset or feature</td><td></td></tr><tr><td>SpatialExtent</td><td>Array</td><td>Coordinates (lat &#x26; long) of the points defining the bounding box of the layer</td><td></td></tr><tr><td>LastUpdated</td><td>Date</td><td>Timestamp of the last update of the layer</td><td></td></tr></tbody></table>

#### **NonSpaatialTableMetadata**&#x20;

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Title of the dataset or feature</td><td></td></tr><tr><td>Abstract</td><td>String</td><td>Abstract description of the dataset or feature</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Author</td><td>String</td><td>Author description</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Keywords</td><td>String</td><td>Keywords associated with the dataset or feature</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>LastUpdated</td><td>Date</td><td>Timestamp of the last update of the table</td><td></td></tr></tbody></table>

#### **GISQuery**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Type</td><td>String {coded_domain}</td><td>Type of the query, either "ad hoc" or "predefined."</td><td></td></tr><tr><td>QueryFormat</td><td>String</td><td>Format of the query (e.g., JSON, XML, SQL).</td><td></td></tr><tr><td>QueryString</td><td>String</td><td>The query expression (e.g., SQL)</td><td></td></tr><tr><td>TimeStamp</td><td>Date</td><td>Date and time when the query was executed or created</td><td></td></tr><tr><td>Name</td><td>String</td><td>Title or description of the query</td><td>Optional (only required for predefined query)</td></tr></tbody></table>

#### **LocationalQuery**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>LayerType</td><td>Geometry</td><td>Type of the queried GIS layers (point, polygon, or line)</td><td></td></tr><tr><td>SpatialRelation</td><td>String {coded_domain}</td><td>Indicates the spatial relationship used in the query (e.g., "intersects," "contains," "within").</td><td></td></tr><tr><td>Longitude</td><td>Real</td><td>Represents the longitude value for the location in the query.</td><td>Optional: Required only if the queried geographic feature is represented by ONE POINT</td></tr><tr><td>Latitude</td><td>Real</td><td>Represents the latitude value for the location in the query.</td><td>Optional: Required only if the queried geographic feature is represented by ONE POINT</td></tr><tr><td>Distance</td><td>Real</td><td>Represents the distance used in the spatial query </td><td>Optional: Required only if the query requires a specification of a distance (e.g., bugger distance) </td></tr></tbody></table>

#### **AttributeQuery**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>AttributeName</td><td>String</td><td>Name of the attribute being queried (e.g., "population," "temperature," "category").</td><td></td></tr><tr><td>Operator</td><td>String</td><td>Indicates the comparison operator used in the attribute query (e.g., "=", ">", "&#x3C;=", "LIKE").</td><td>The values for this attribute should follow the standard comparison operators</td></tr><tr><td>Value</td><td>String or Numeric</td><td>Represents the value used in the attribute query for comparison.</td><td>The data type of the Value attribute should match the data type of the attribute being queried. For example, if the AttributeName is "population" and the population values are stored as integers, the Value should also be of integer data type.</td></tr></tbody></table>

**DiscoveryQuery**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>AttributeName</td><td>String</td><td>Contains the keywords or search terms used for discovering metadata information</td><td>This attribute will typically store a comma-separated list of keywords or a single string representing the search terms.</td></tr></tbody></table>

**QueryResult**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>QueryType</td><td>String {coded_domain}</td><td>The type of query that generated this result </td><td>Coded values will include "Locational Query," "Attribute Query," and "Metadata Discovery Query,"</td></tr><tr><td>QueryStatus</td><td>String {coded_domain}</td><td>Represents the status of the query result</td><td>Possible values could be "Success," "Partial Result," "No Results Found," "Error," etc.</td></tr><tr><td>TimeStamp</td><td>Date</td><td>Represents the date and time when the query result was generated</td><td></td></tr></tbody></table>

### 7.2.3 Group: GIS Data Management

#### **DataStore**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Name or label of the GIS datastore</td><td></td></tr><tr><td>Description</td><td>String</td><td>A detailed description of the GIS data store</td><td></td></tr><tr><td>Provider</td><td>String</td><td>Provider or source of the GIS data store</td><td></td></tr><tr><td>ConnectionString</td><td>String</td><td>Connection string required to access the GIS data store</td><td></td></tr><tr><td>AccessRestrictions</td><td>Boolean</td><td>Enable or disable access restrictions or permissions required to use the GIS data store</td><td></td></tr><tr><td>UpdateFrequency</td><td>String</td><td>Description of how often the GIS data store is updated or refreshed with new data</td><td></td></tr></tbody></table>

#### **DataStoreMetadata**

<table><thead><tr><th width="166">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Title of the datastore </td><td></td></tr><tr><td>Source</td><td>String</td><td>Source/Publisher of the datastore </td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Description</td><td>String</td><td>Description of the datastore</td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>Keywords</td><td>String</td><td>Keywords associated with the datastore </td><td>Must adheres to ISO 19115:2014 Standard pm GI Metadata <a href="https://www.iso.org/standard/53798.html">https://www.iso.org/standard/53798.html</a></td></tr><tr><td>LastUpdated</td><td>Date</td><td>Timestamp of the last publishing date of the datastore</td><td></td></tr></tbody></table>

#### **UserControl**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Username</td><td>String</td><td>Username for authentication</td><td></td></tr><tr><td>Password</td><td>String</td><td>The password associated with the username for authentication to the GIS data store</td><td></td></tr><tr><td>EditorPermissions</td><td><p>String</p><p>{coded_value}</p></td><td>Codes depicting access control level over editing capabilities provided by the service (view, edit, delete, no edits)</td><td></td></tr><tr><td>EditorTracking</td><td>Boolean</td><td>Whether or not it should record who created or updated features and when they did it (providing accountability for the edits)</td><td>Optional</td></tr><tr><td>OwnerControl</td><td>Boolean</td><td>Limits access to geographic features based on who created them.</td><td>Optional</td></tr></tbody></table>

#### EditorTracking

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>EditType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of editing operation (create, update, delete)</td><td></td></tr><tr><td>TimeStamp</td><td>String</td><td>Timestamp indicating when the edit was made</td><td></td></tr></tbody></table>

#### **Replica**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>SourceDataStore</td><td>String {url}</td><td>Links the replica to the source GIS Datastore.</td><td></td></tr><tr><td>TargetDataStore</td><td>String {url}</td><td>Links the replica to the target GIS Datastore.</td><td></td></tr><tr><td>ReplicaType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of replica operation (creation, synchronization, extraction).</td><td></td></tr></tbody></table>

### 7.2.4 Geocoding and Reverse Geocoding

#### **AddressData**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Address</td><td>String</td><td>Address information for geocoding or reverse geocoding.</td><td></td></tr><tr><td>Latitude</td><td>Real</td><td>Latitude coordinate for the address </td><td>Used for Reverse Geocoding</td></tr><tr><td>Longitude</td><td>Real</td><td>Longitude coordinate for the address </td><td>Used for Reverse Geocoding</td></tr></tbody></table>

#### **AddressAlias**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Alias</td><td>String</td><td>Alias or potential alternative address for the Address Data</td><td>An address may have <em>0</em> to <em>n</em> aliases</td></tr></tbody></table>

#### **AddressFormat**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>FormatingName</td><td>String</td><td>Name of the address format</td><td></td></tr><tr><td>CountryCode</td><td><p>String</p><p>{coded_value}</p></td><td>Country code for the address format</td><td>Optional</td></tr><tr><td>FormatString</td><td>String</td><td>Format string representing the structure of the address</td><td></td></tr></tbody></table>

#### **GeocodingBatch**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>BatchType</td><td><p>String</p><p>{coded_value}</p></td><td>Code representing whether the batch performs geocoding or reverse geocoding</td><td></td></tr><tr><td>BatchName</td><td>String</td><td>Name of the geocoding batch</td><td></td></tr><tr><td>Status</td><td><p>String</p><p>{coded_value}</p></td><td>Status of the geocoding batch (e.g., processing, completed)</td><td></td></tr><tr><td>TimeStamp</td><td>Date</td><td>Date and time of when the geocoding batch was completed.</td><td></td></tr></tbody></table>

### 7.2.5 Spatial Awareness and Analysis

#### **Geoprocessing**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="206">Description</th><th>Notes</th></tr></thead><tbody><tr><td>ProcessingName</td><td>String</td><td>Name of the geoprocessing task</td><td></td></tr><tr><td>Description</td><td>String</td><td>Detailed information that describes the geoprocessing task</td><td></td></tr><tr><td>Parameters</td><td>Array</td><td>Array of input and output parameters that are needed to execute the geoprocessing job (parameter name, value, code represents whether it is input or output parameter, and default value)</td><td>Refer to OGC API Processes: <a href="https://ogcapi.ogc.org/processes/">https://ogcapi.ogc.org/processes/</a></td></tr></tbody></table>

#### **ExecustionStatus**

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Status</td><td><p>String</p><p>{coded_value}</p></td><td>Status of the geoprocessing task execution (e.g., running, completed)</td><td></td></tr><tr><td>StartTime</td><td>Date</td><td>Timestamp indicating the start time of the geoprocessing task execution</td><td></td></tr><tr><td>EndTime</td><td>Date</td><td>Timestamp indicating the end time of the geoprocessing task execution</td><td></td></tr><tr><td>Result</td><td>Object</td><td>Result of the geoprocessing task execution</td><td>GIS layers, attributes, or information generated when executed successfully</td></tr></tbody></table>

### 7.2.6 Reporting

#### MapReport

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Title/name of the map report</td><td></td></tr><tr><td>Abstract</td><td>String</td><td>A brief summary or abstract of the map report and its purpose</td><td></td></tr><tr><td>Author</td><td>String</td><td>The name of the author or creator of the report.</td><td></td></tr><tr><td>Keywords</td><td>String</td><td>Keywords or tags associated with the report.</td><td></td></tr><tr><td>LastUpdated</td><td>Date</td><td>The date and time when the report was created or last updated.</td><td></td></tr></tbody></table>

#### ReportQueue

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Status</td><td><p>String</p><p>{coded_value}</p></td><td>Status of the report in the queue (e.g., pending, processing, completed).</td><td></td></tr><tr><td>Priority</td><td><p>String</p><p>{coded_value}</p></td><td>The priority level of the report in the queue (high, normal, low)</td><td></td></tr><tr><td>Recurring</td><td>Boolean</td><td>Indicates if the report is a recurring task</td><td></td></tr><tr><td>Interval</td><td>String</td><td>Time interval for recurring reports </td><td>Active only when Recurring is True</td></tr><tr><td>StartTime</td><td>Date</td><td>Timestamp indicating the start time of the report processing</td><td></td></tr><tr><td>EndTime</td><td>Date</td><td>Timestamp indicating the end time of the report processing</td><td></td></tr></tbody></table>

#### ReportResource

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>ResourceName</td><td>String</td><td>Name of the Resource</td><td></td></tr><tr><td>ResourceType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of the Resource (e.g., symbology, charts, north arrows, scale bar, etc.)</td><td></td></tr></tbody></table>

#### Symbology

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>SymbolType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of the symbol (e.g., Dot Density Maps, Graduated Color, Graduated/Proportional Symbol, etc.)</td><td></td></tr><tr><td>SymbolColor</td><td><p>String</p><p>{coded_value}</p></td><td>Color code of  the symbol</td><td></td></tr><tr><td>Transparency</td><td>Float</td><td>Transparency level of the symbol</td><td></td></tr></tbody></table>

#### Label

<table><thead><tr><th width="206">Field</th><th width="168">Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>LabelText</td><td>String</td><td>Text of the Label</td><td></td></tr><tr><td>PositionX</td><td>Real</td><td>X-coordinate position of the Label on the map report</td><td></td></tr><tr><td>PositionY</td><td>Real</td><td>Y-coordinate position of the Label on the map report</td><td></td></tr><tr><td>Font</td><td><p>String</p><p>{coded_value}</p></td><td>Font of the Label</td><td></td></tr><tr><td>Size</td><td>Integer</td><td>Size of the Label</td><td></td></tr><tr><td>Color</td><td><p>String</p><p>{coded_value}</p></td><td>Color of the Label</td><td></td></tr></tbody></table>

#### Chart

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Title of the chart</td><td></td></tr><tr><td>Type</td><td><p>String</p><p>{coded_value}</p></td><td>Type of the chart (e.g., bar chart, histogram, etc.)</td><td></td></tr><tr><td>Data</td><td>Blob</td><td>Data of the chart</td><td></td></tr></tbody></table>

#### Legend

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Name of the Legend</td><td></td></tr><tr><td>PositionX</td><td>Real</td><td>X-coordinate position of the Legend on the map</td><td></td></tr><tr><td>PositionY</td><td>Real</td><td>Y-coordinate position of the Legend on the map</td><td></td></tr><tr><td>Font</td><td><p>String</p><p>{coded_value}</p></td><td>Font of the Legend</td><td></td></tr><tr><td>Size</td><td>Integer</td><td>Size of the Legend font</td><td></td></tr><tr><td>Color</td><td><p>String</p><p>{coded_value}</p></td><td>Color of the Legend</td><td></td></tr></tbody></table>

#### ScaleBar

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Name of the scale bar</td><td></td></tr><tr><td>Style</td><td><p>String</p><p>{coded_value}</p></td><td>Type and style of the scale bar (linear, graphic, etc.)</td><td></td></tr><tr><td>Length</td><td>Float</td><td>Length of the scale bar on the map report</td><td></td></tr><tr><td>Units</td><td>String</td><td>Units of measurement for the scale bar</td><td></td></tr><tr><td>PositionX</td><td>Real</td><td>X-coordinate position of the scale bar on the map</td><td></td></tr><tr><td>PositionY</td><td>Real</td><td>Y-coordinate position of the scale bar on the map Legend on the map</td><td></td></tr><tr><td>Font</td><td><p>String</p><p>{coded_value}</p></td><td>Font of the Scale Bar</td><td></td></tr><tr><td>Size</td><td>Integer</td><td>Size of the Scale Bar</td><td></td></tr><tr><td>Color</td><td><p>String</p><p>{coded_value}</p></td><td>Color of the Scale Bar</td><td></td></tr></tbody></table>

#### NorthArrow

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Title</td><td>String</td><td>Name of the north arrow</td><td></td></tr><tr><td>Style</td><td><p>String</p><p>{coded_value}</p></td><td>Type and style of the north arrows (simple, arrow with N, etc.)</td><td></td></tr><tr><td>Length</td><td>Float</td><td>Length of the North Arrow on the map report</td><td></td></tr><tr><td>Units</td><td>String</td><td>Units of measurement for the north arrow</td><td></td></tr><tr><td>PositionX</td><td>Real</td><td>X-coordinate position of the north arrow on the map</td><td></td></tr><tr><td>PositionY</td><td>Real</td><td>Y-coordinate position of the north arrow on the map</td><td></td></tr><tr><td>Font</td><td><p>String</p><p>{coded_value}</p></td><td>Font of the North Arrow</td><td></td></tr><tr><td>Size</td><td>Integer</td><td>Size of the North Arrow</td><td></td></tr><tr><td>Color</td><td><p>String</p><p>{coded_value}</p></td><td>Color of the North Arrow</td><td></td></tr></tbody></table>

### 7.2.7 Gefencing

#### Geofence

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Name</td><td>String</td><td>Name of the Geofence</td><td></td></tr><tr><td>Shape</td><td><p>String</p><p>{coded_value}</p></td><td>Shape of the Geofence (e.g., circle, polygon).</td><td></td></tr><tr><td>Size</td><td>Float</td><td>Size of the Geofence, representing the radius for a circular Geofence or the area for a polygon Geofence</td><td></td></tr><tr><td>Status</td><td>Boolean</td><td>Indicates if the Geofence is activated or deactivated</td><td></td></tr></tbody></table>

#### GefenceElement

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>ElementType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of the tracked element (e.g., vehicle, device, asset, person).</td><td></td></tr><tr><td>TrackingMethod</td><td><p>String</p><p>{coded_value}</p></td><td>Method of tracking (GPS Coordinates, RFID tags, etc.)</td><td></td></tr></tbody></table>

#### ActionRule

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>ActionType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of action to be performed (e.g., send notification, execute command).</td><td></td></tr><tr><td>Action</td><td><p>String</p><p>{coded_value}</p></td><td>Description and details or parameters related to the action</td><td></td></tr></tbody></table>

#### Geofence Notification

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>NotificationType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of notification (e.g., push notification, SMS, email).</td><td></td></tr><tr><td>Recipient</td><td>String</td><td>Recipient's contact information (e.g., email address, phone number).</td><td></td></tr><tr><td>RecipientType</td><td><p>String</p><p>{coded_value}</p></td><td>Type of recipient (e.g., user, group)</td><td></td></tr></tbody></table>

### 7.2.8 Routing

#### Route

<table><thead><tr><th width="213">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>StartNode</td><td>Object</td><td>Geographic feature representing the starting point of the route</td><td></td></tr><tr><td>EndNode</td><td>Object</td><td>Geographic feature representing the ending point of the route</td><td></td></tr><tr><td>PassThrough</td><td>Boolean</td><td>Indicates whether the route should pass through intermediate points</td><td></td></tr><tr><td>Restrictions</td><td>String</td><td>Specifies any restrictions or obstacles to avoid along the route</td><td></td></tr><tr><td>AdditionalParameters</td><td>String</td><td>Additional routing rules and parameters for the route</td><td></td></tr></tbody></table>

#### RouteNode

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Latitude</td><td>Real</td><td>Latitude coordinate of the node</td><td></td></tr><tr><td>Longitude</td><td>Real</td><td>Longitude coordinate of the node</td><td></td></tr><tr><td>Order</td><td>Integer</td><td>Order of the node in the route sequence</td><td></td></tr></tbody></table>

#### RouteSegment

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>StartNode</td><td>Object</td><td>Geographic feature representing the starting point of the route segment</td><td></td></tr><tr><td>EndNode</td><td>Object</td><td>Geographic feature representing the ending point of the route segment</td><td></td></tr><tr><td>Length</td><td>Float</td><td>Length of the route segment</td><td></td></tr></tbody></table>

#### ServiceArea

<table><thead><tr><th width="206">Field</th><th>Type</th><th width="205">Description</th><th>Notes</th></tr></thead><tbody><tr><td>Shape</td><td><p>String</p><p>{coded_value}</p></td><td>Shape of the service area (e.g., circle, polygon).</td><td></td></tr><tr><td>Size</td><td>Float</td><td>Size of the service area, representing the radius for a circular service area or the area for a polygon </td><td></td></tr></tbody></table>
