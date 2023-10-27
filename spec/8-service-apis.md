---
description: >-
  This section provides a reference for APIs that should be implemented by this
  Building Block.
---

# 8 Service APIs

This section provides a reference for the APIs implemented by the GIS Building Block. The APIs defined here establish a blueprint for how the Building Block will interact with other Building Blocks. Additional APIs may be implemented by the Building Block, but the listed APIs define a minimal set of functionality that should be provided by any implementation of this Building Block.&#x20;

The GIS BB APIs conform with the [OGC web API principles and guidelines](https://github.com/opengeospatial/OGC-Web-API-Guidelines) and should be deployed as a set of microservices to provide clients consistent access to the key digital functionalities and geographic data in different representations. Microservices are defined to receive requests with relevant inputs and return processed results from key digital functionalities of this Building Block. Microservices are small, independent, and loosely coupled services that perform specific functions within the larger GIS BB key digital functionalities. Each microservice is kept simple and intuitive by focusing on one particular task, and together they form a cohesive and scalable GIS architecture. Each microservice can be developed, deployed, and maintained independently, making it easier to manage and scale the system as needed.

This section provides a reference for APIs that this Building Block should implement. The APIs defined here establish a blueprint for how the Building Block will interact with other Building Blocks. The Building Block may implement additional APIs, but the listed APIs define a minimal set of functionality that any implementation of this Building Block should provide.&#x20;

The [GovStack non-functional requirements document](https://govstack.gitbook.io/specification/architecture-and-nonfunctional-requirements/6-onboarding) provides additional information on how 'adaptors' may be used to translate an existing API to the patterns described here.

### 8.1 Map Display

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/type" method="get" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/details" method="get" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/bookmarks" method="post" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/scale" method="put" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/navigation" method="put" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/notes" method="post" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/measuring" method="post" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml" path="/style" method="get" %}
[GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_mapDisplay-1.0.0-swagger-2.yaml)
{% endswagger %}

### 8.2 GIS Query&#x20;

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/layerMetadata" method="get" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/nonSpatialTableMetadata" method="get" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/gisQuery" method="post" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/locationalQuery" method="post" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/attributeQuery" method="post" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/discoveryQuery" method="post" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml" path="/queryResult" method="get" %}
[GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_queryGIS-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.3 GIS Data Management&#x20;

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/dataStore" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/dataStore/{dataStoreId}" method="get" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/dataStore/{dataStoreId}" method="patch" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/dataStoreMetadata" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/userControl" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/editorTracking" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/replicate" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/extractTransfer" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml" path="/editFeature" method="post" %}
[GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_dataManagement-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.4 Geocoding and Reverse Geocoding

{% swagger src=".gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml" path="/geocode" method="post" %}
[GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml" path="/reverseGeocode" method="post" %}
[GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml" path="/batchGeocode" method="post" %}
[GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml" path="/geocodeResult/{resultId}" method="get" %}
[GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml" path="/reverseGeocodeResult/{resultId}" method="get" %}
[GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geocodingReverseGeocoding-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.5 Spatial Awareness and Analysis

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/metadata" method="get" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/processes" method="get" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/executeTask" method="post" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/taskStatus/{taskId}" method="get" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/taskResult/{taskId}" method="get" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml" path="/terminateTask/{taskId}" method="post" %}
[GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_spatialAwarenessAnalysisg-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.6 Reporting

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/templates" method="get" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/dynamicLayers" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/dynamicLayers/{layerId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/labels" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/labels/{labelId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/charts" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/charts/{chartId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/legends" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/legends/{legendId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/scaleBars" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/scaleBars/{scaleBarId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/northArrows" method="post" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml" path="/northArrows/{northArrowId}" method="delete" %}
[GovStack_GISBB_reporting-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_reporting-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.7 Geofencing

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences" method="get" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}" method="get" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}" method="put" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}" method="delete" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/status" method="get" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/activate" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/deactivate" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/elements" method="get" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/elements" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/elements/{elementId}" method="delete" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/rules" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml" path="/geofences/{geofenceId}/elements/{elementId}/actions" method="post" %}
[GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_geofencing-1.1.0-swagger-2.yaml)
{% endswagger %}

### 8.8 Routing

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/routes" method="post" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/routes/{routeId}" method="get" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/routes/{routeId}" method="delete" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/routes/{routeId}/directions" method="get" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/routes/{routeId}/segments" method="get" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml" path="/service-areas" method="get" %}
[GovStack_GISBB_routing-1.1.0-swagger-2.yaml](.gitbook/assets/GovStack_GISBB_routing-1.1.0-swagger-2.yaml)
{% endswagger %}
