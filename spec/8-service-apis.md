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

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml" path="/discovery/metadata/{layerId}" method="get" %}
[TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml" path="/discovery/feature-types/{layerId}" method="get" %}
[TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml" path="/query/interactive" method="post" %}
[TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml)
{% endswagger %}

{% swagger src=".gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml" path="/query/predefined/{queryId}" method="get" %}
[TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml](.gitbook/assets/TAREK_3-GovStack_GIS_BB_GISQuery_API-1.0.0-resolved.yaml)
{% endswagger %}
