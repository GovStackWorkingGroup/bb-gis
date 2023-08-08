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

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/type" method="get" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/details" method="get" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/bookmarks" method="post" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/scale" method="put" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/navigation" method="put" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/notes" method="post" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/measuring" method="post" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml" path="/style" method="get" %}
[TAREK_3-MapDisplay-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-MapDisplay-1.0.0-swagger.yaml)
{% endswagger %}

### 8.2 GIS Query&#x20;

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/layer-metadata" method="get" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/non-spatial-table-metadata" method="get" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/gis-query" method="post" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/locational-query" method="post" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/attribute-query" method="post" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/discovery-query" method="post" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml" path="/query-result" method="get" %}
[TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISQuery-1.0.0-swagger.yaml)
{% endswagger %}

### 8.3 GIS Data Management&#x20;

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/data-store" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/data-store/{dataStoreId}" method="get" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/data-store/{dataStoreId}" method="patch" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/data-store-metadata" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/user-control" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/editor-tracking" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/replicate" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/extract-transfer" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml" path="/edit-feature" method="post" %}
[TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GISBB_GISDataManagement-1.0.0-resolved.yaml)
{% endswagger %}

### 8.4 Geocoding and Reverse Geocoding

{% swagger src=".gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml" path="/geocode" method="post" %}
[GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml" path="/reverse-geocode" method="post" %}
[GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml" path="/batch-geocode" method="post" %}
[GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml" path="/geocode-result/{resultId}" method="get" %}
[GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml" path="/reverse-geocode-result/{resultId}" method="get" %}
[GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geocoding_and_ReverseGeocoding-1.0.0-swagger.yaml)
{% endswagger %}

### 8.5 Spatial Awareness and Analysis

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/metadata" method="get" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/processes" method="get" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/execute-task" method="post" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/task-status/{taskId}" method="get" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/task-result/{taskId}" method="get" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml" path="/terminate-task/{taskId}" method="post" %}
[GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_SpatialAnalysis_and_Awareness-1.0.0-swagger.yaml)
{% endswagger %}

### 8.6 Reporting

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/templates" method="get" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/dynamic-layers" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/dynamic-layers/{layerId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/labels" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/labels/{labelId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/charts" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/charts/{chartId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/legends" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/legends/{legendId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/scale-bars" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/scale-bars/{scaleBarId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/north-arrows" method="post" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml" path="/north-arrows/{northArrowId}" method="delete" %}
[GovStack_GISBB_Reporting-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Reporting-1.0.0-swagger.yaml)
{% endswagger %}

### 8.7 Geofencing

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences" method="get" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}" method="get" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}" method="put" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}" method="delete" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/status" method="get" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/activate" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/deactivate" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/elements" method="get" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/elements" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/elements/{elementId}" method="delete" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/rules" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml" path="/geofences/{geofenceId}/elements/{elementId}/actions" method="post" %}
[GovStack_GISBB_Geofencing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Geofencing-1.0.0-swagger.yaml)
{% endswagger %}

### 8.8 Routing

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/routes" method="post" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/routes/{routeId}" method="get" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/routes/{routeId}" method="delete" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/routes/{routeId}/directions" method="get" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/routes/{routeId}/segments" method="get" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml" path="/service-areas" method="get" %}
[GovStack_GISBB_Routing-1.0.0-swagger.yaml](.gitbook/assets/GovStack_GISBB_Routing-1.0.0-swagger.yaml)
{% endswagger %}
