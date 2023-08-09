---
description: >-
  This section provides a detailed view of how this Building Block will interact
  with other Building Blocks to support common use cases.
---

# 9 Internal Workflows

The following internal workflows describe the processes the GIS Building Block executes to fulfill a request from an external application or Building Block to meet the functional requirements stated in Section 6 of this specification. In the current scope, examples are drawn from the user-journey steps of the use-cases of the GIS-Based Incident Management System and Land Records/Cadaster Management provided in Section 2. The below common preconditions should be met before utilizing the GIS BB Services:

* **Information Mediator BB Configuration**: All the service endpoints of the GIS BB APIs should be configured in the Information Mediator BB.
* **Conformance to Open Standards:** Developers of the GIS BB APIs should adhere to the [OGC web API guidelines and principles](https://github.com/opengeospatial/OGC-Web-API-Guidelines), and Cross-Origin Resource Sharing (CORS) to enable seamless integration and data exchange of GIS data between GIS BB APIs and GIS API services offered by other systems.
* **Data Format Compatibility:** The geospatial data source handled by the GIS BB APIs, whether vector data (points, lines, and polygons) or raster data (imagery, elevation data), should be in a format compatible with the specific API used (e.g., GeoJSON, GML, KML, etc.) per Section 7 of this specification.
* **Coordinate System Awareness:** Developers and users should understand the coordinate system and projections used in their geospatial data to prevent inaccuracies in analysis and visualization.
* **No Authentication or API Keys:** As a general rule, developers of the GIS BB APIs should avoid mandatory authentication mechanisms or API keys that can limit access; make the API accessible to anyone without a signup process unless there is a legitimate requirement to impose authentication mechanisms.

### 9.1 GIS Map Display

#### 9.1.1 Interactions between an external application or a Building Block and the MapDisplay API with data store integration

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

```mermaid
sequenceDiagram
  participant ExternalApp as External Application
  participant MapDisplayAPI as Map Display API
  participant DataStore as Data Store

  ExternalApp->>+MapDisplayAPI: Request Map Display Details
  Note over MapDisplayAPI: ExternalApp requests map display details

  MapDisplayAPI->>+DataStore: Retrieve Data for Display
  Note over DataStore: MapDisplayAPI fetches data from the Data Store

  DataStore-->>-MapDisplayAPI: Return Data for Display
  Note over DataStore: Data Store provides requested data to MapDisplayAPI

  MapDisplayAPI->>+MapDisplayAPI: Prepare Map Display Details
  Note over MapDisplayAPI: API prepares map display details based on data viewer type

  MapDisplayAPI->>-ExternalApp: Respond with Map Display Details
  Note over ExternalApp: MapDisplayAPI provides tailored map display details

  ExternalApp->>+MapDisplayAPI: Request Layer ToC
  Note over ExternalApp: ExternalApp requests layer Table of Contents

  MapDisplayAPI->>-ExternalApp: Respond with Layer ToC
  Note over MapDisplayAPI: MapDisplayAPI provides layer Table of Contents

  ExternalApp->>+MapDisplayAPI: Request Turn On/Off Specific Layer
  Note over ExternalApp: ExternalApp requests to turn on/off a specific layer

  MapDisplayAPI->>-ExternalApp: Respond with Layer Status
  Note over MapDisplayAPI: MapDisplayAPI provides layer status

  ExternalApp->>+MapDisplayAPI: Request Turn On/Off All Layers
  Note over ExternalApp: ExternalApp requests to turn on/off all layers

  MapDisplayAPI->>-ExternalApp: Respond with All Layers Status
  Note over MapDisplayAPI: MapDisplayAPI provides all layers status

  ExternalApp->>+MapDisplayAPI: Request Add Bookmark
  Note over ExternalApp: ExternalApp requests to add a bookmark

  MapDisplayAPI->>-ExternalApp: Respond with Bookmark Status
  Note over MapDisplayAPI: MapDisplayAPI provides bookmark status

  ExternalApp->>+MapDisplayAPI: Request Update Layer Scale
  Note over ExternalApp: ExternalApp requests to update layer scale

  MapDisplayAPI->>-ExternalApp: Respond with Scale Update Status
  Note over MapDisplayAPI: MapDisplayAPI provides scale update status

  ExternalApp->>+MapDisplayAPI: Request Basic Navigation
  Note over ExternalApp: ExternalApp requests basic navigation

  MapDisplayAPI->>-ExternalApp: Respond with Navigation Status
  Note over MapDisplayAPI: MapDisplayAPI provides navigation status

  ExternalApp->>+MapDisplayAPI: Request Add Map Note
  Note over ExternalApp: ExternalApp requests to add a map note

  MapDisplayAPI->>-ExternalApp: Respond with Map Note Status
  Note over MapDisplayAPI: MapDisplayAPI provides map note status

  ExternalApp->>+MapDisplayAPI: Request Measuring Action
  Note over ExternalApp: ExternalApp requests measuring action

  MapDisplayAPI->>-ExternalApp: Respond with Measuring Status
  Note over MapDisplayAPI: MapDisplayAPI provides measuring status

  ExternalApp->>+MapDisplayAPI: Request Data Viewer Style
  Note over ExternalApp: ExternalApp requests data viewer style

  MapDisplayAPI->>-ExternalApp: Respond with Data Viewer Style
  Note over MapDisplayAPI: MapDisplayAPI provides data viewer style
```

#### 9.1.1  Example 1: Cadastral User Displaying Land Use and Title Layers with Parcel Zoom



<figure><img src=".gitbook/assets/mermaid-diagram-2023-08-09-132625.png" alt=""><figcaption></figcaption></figure>

```mermaid
sequenceDiagram
  participant ExternalApp as "Cadastral User"
  participant MapDisplayAPI as "MapDisplay API"
  participant DataStore as "Data Store"

  ExternalApp ->> MapDisplayAPI: Request Map Display Details
  MapDisplayAPI ->> ExternalApp: Provide Map Display Details
  Note over MapDisplayAPI: Title: Cadastral Map\nAttribution: Cadastral Department\nCenter: 45.6789, -123.4567\nBounds: 45.1234, -124.5678 to 46.7890, -122.3456\nVisible Layers: Land Use, Titles

  ExternalApp ->> MapDisplayAPI: Request Land Use Layer
  MapDisplayAPI ->> DataStore: Retrieve Land Use Data
  DataStore -->> MapDisplayAPI: Provide Land Use Layer Data
  MapDisplayAPI ->> ExternalApp: Provide Land Use Layer Data
  Note over MapDisplayAPI: Land Use Layer Data\nExample: { "type": "FeatureCollection", "features": [ ... ] }

  ExternalApp ->> MapDisplayAPI: Request Title Records Layer
  MapDisplayAPI ->> DataStore: Retrieve Title Records Data
  DataStore -->> MapDisplayAPI: Provide Title Records Layer Data
  MapDisplayAPI ->> ExternalApp: Provide Title Records Layer Data
  Note over MapDisplayAPI: Title Records Layer Data\nExample: { "type": "FeatureCollection", "features": [ ... ] }

  ExternalApp ->> MapDisplayAPI: Zoom to Parcel
  MapDisplayAPI -->> ExternalApp: Parcel Zoomed In
  Note over MapDisplayAPI: Zoomed to Parcel ID: 12345

```

#### 9.1.2  Example 2: Emergency Dispatcher: Accident Location Bookmarking and Map Note Addition

<figure><img src=".gitbook/assets/mermaid-diagram-2023-08-09-135106.png" alt=""><figcaption></figcaption></figure>

```mermaid
sequenceDiagram
  participant Dispatcher as "Emergency Dispatcher"
  participant MapDisplayAPI as "MapDisplay API"
  participant DataStore as "Data Store"

  Dispatcher ->> MapDisplayAPI: Request Accident Location
  MapDisplayAPI ->> DataStore: Retrieve Accident Location Data
  DataStore -->> MapDisplayAPI: Provide Accident Location Data
  MapDisplayAPI ->> Dispatcher: Provide Accident Location Data

  Note over MapDisplayAPI: Accident Location Details\nLatitude: 40.7128\nLongitude: -74.0060

  Dispatcher ->> MapDisplayAPI: Bookmark Accident Location
  MapDisplayAPI ->> DataStore: Save Bookmark
  DataStore -->> MapDisplayAPI: Bookmark Saved
  MapDisplayAPI -->> Dispatcher: Bookmark Created

  Note over MapDisplayAPI: Bookmark: Accident Location

  Dispatcher ->> MapDisplayAPI: Add Note about Accident Type
  MapDisplayAPI ->> DataStore: Save Note
  DataStore -->> MapDisplayAPI: Note Saved
  MapDisplayAPI -->> Dispatcher: Note Added

  Note over MapDisplayAPI: Accident Type: Vehicle Collision

```
