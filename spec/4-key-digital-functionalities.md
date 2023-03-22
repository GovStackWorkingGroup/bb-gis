# 4 Key Digital Functionalities

{% hint style="success" %}
The Key Digital Functionalities describe the core (required) functions that this building block must be able to perform. These functionalities should be described as business processes as opposed to technical specifications or API definitions.

Note, this section may be extended after the key functionalities have been listed to include any assumptions or context that is needed. Additionally, if the Building Block contains multiple components, the functionalities for each may be described.
{% endhint %}



## **The current scope of functionalities considered of this BB**

* The determination of the GIS BB functionalities relies on reviewing two specific use cases of Incident management system and Cadastral/Land Information Management.



### Key Functionalities:

&#x20;  The GIS BB provides the following key digital functionalities to support geographic information services:

* **Map Display**: A Map Display service dynamically produces maps of spatially referenced data from geographic information. suitable for display on a computer screen following OGC Web Services Context (OWS) standard. The Map Display service described here conforms to and satisfies all the requirements of the following OGC standards, including queryable Web Mapping Service (WMS), Web Feature Service (WFS), Web Map Tile Service (WMTS), Web Coverage Service (WCS), Web Processing Service (WPS),  and Geopackage.
* **GIS Query**: This functionality provides services to create, modify, and query GIS data through two distinct types of query operations. Discovery operations enable clients to retrieve metadata about the feature collections in the GIS dataset. Query operations allow clients to retrieve actual features from the underlying data store based on selection criteria defined by the client through standard SQL language or spatial predicates. The services described below conform to and satisfy all the requirements of the following OGC and ISO standards, including queryable Web Mapping Service (WMS), Web Feature Service (WFS), Web Feature Service (WFS), Web Feature Service (WFS) Temporality Extension, Web Feature Service 2.0 Interface Standard, OGC API – Features, and ISO 19168-1: 2020.
* GIS Layer Management
* Geocoding
* Tabular Information Manipulation
* Spatial Awareness and Analysis
* Reporting
* Geofencing&#x20;
* Routing
* Resource Tracking
