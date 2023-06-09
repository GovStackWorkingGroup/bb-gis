---
description: This section provides context for this Building Block.
---

# 2 Description

Geospatial information represents Earth’s features: maps, images, addresses, zip codes, phone numbers, landmarks, events, etc. Location and time are foundational properties of geographic information, providing a unifying theme to understand the context of most real and abstract phenomena.

The GIS (geographic information services) building block enables various applications with location-based capabilities. Integrating a wide range of spatial data, such as maps, imagery, and location-based services, allows users to access and process geospatial data from different sources and link geographic locations to various "objects." within an open information technology environment For example, users can link geographic locations to people, such as patients, doctors, farmers, and agricultural extension practitioners. They can also link geographic locations to hospitals, ambulances, labs, seed production facilities, etc. Additionally, equipment such as ventilators and vaccine containers can be linked to geographic locations, as can sites like water sources and agricultural fields. This geographic association can also be tagged with a unique digital identifier and a timestamp of when it was acquired.

Applications or components using geographical information services can collect, share, and use temporal and spatial information with other applications, such as map repositories and data visualization tools. These tools can display the collected information on geographical maps, giving users a powerful visual representation of the data. Furthermore, the collected data can be combined with other datasets, such as population, surveillance, or supply chain data sets, to enable interoperable geospatial and spatiotemporal analysis. This can help to identify patterns and trends in the data that might not otherwise be apparent.

Below are a few examples of the many sectors that can benefit from GIS services and applications:

* **Local government:** cadastral mapping and management, land use and transportation planning, and optimization of services delivery such as postal services, trash collection, etc.
* **Incident Management and Emergency Response**: call services, dispatching, tracking emergency vehicles and resources, redlining, etc.
* **Law enforcement:** tracking crime patterns, investigating crimes, and public safety planning
* **Natural resources:** managing water resources, monitoring forests, and conservation planning
* **Planning:** planning for development, transportation, and other infrastructure projects.
* **Agriculture:** tracking crop yields, providing weather information for farmers, planning for agricultural development, and precision farming.
* **Business:** tracking assets and customer shopping habits, analyzing store locations, and supply chain management.
* **Construction:** planning construction projects, tracking progress, and identifying potential hazards.
* **Energy:** management of energy resources, planning for green energy development, and monitoring energy use.
* **Environment:** measuring pollution, monitoring wildlife populations, and environmental protection.
* **Healthcare:** managing disease outbreaks, planning for healthcare facilities, and improving access to patient care.
* **Risk management:** modeling hazards, exposure, vulnerability analysis, and risk assessment and management.
* **Transportation:** planning transportation routes, tracking traffic, and improving public transportation.
* **Utilities:** utility infrastructure management, customer data management, and utility expansion planning.

## 2.1 **Current scope**

The functional requirements to cover the services required from the GIS Building Block currently consider the specific use cases of:

* GIS-Based Incident Management System ([https://govstack-global.atlassian.net/wiki/spaces/GH/pages/254017537](https://govstack-global.atlassian.net/wiki/spaces/GH/pages/254017537))
* Land Records/Cadastre Management ([https://govstack-global.atlassian.net/wiki/spaces/GH/pages/254181377](https://govstack-global.atlassian.net/wiki/spaces/GH/pages/254181377))

These two use cases cover a wide range of GIS services, including core functionality such as GIS data access, display, and visualization, GIS data query, GIS layer management and manipulation, metadata and cataloging services, locational analysis, geocoding, and reporting. The endless combination of these GIS services can be used to respond to the needs of various applications across many domains and sectors, as listed above.

The following actors have been identified as "users" of the GIS Building Block:

* "**GIS Data Viewer**": displays and views spatial data to find information about a particular location, compare different datasets, or create spatial data visualizations.
* "**GIS Data Editor**": performs spatial data editing by adding, updating, or deleting geographic data features from a dataset or changing the properties and attributes of these features.
* "**GIS Admin**": manages GIS data by creating, maintaining, and organizing geographic datasets and ensuring that data is accurate and up-to-date.
* "**GIS Application Developer**": develops GIS applications by deploying one or more GIS BB services to serve business needs.
* "**Discovery Tools**": search for metadata about spatial data to find information about the content of a dataset, the creators of a dataset, or the methods used to create a dataset.
* "**Other Buildings Blocks and Application**": display and consume GIS services to perform specific GIS operations such as creating maps, generating reports, and more.

The GIS BB services MUST enable these actors to perform basic functions and tasks associated with their role as follows:

**2.1.1. The GIS BB MUST enable GIS Data Viewers to**

* view, explore, and analyze spatial data and interact with a wide range of spatial data (including vector maps, raster imagery, and address coordinates).
* explore information about a particular location and interact with spatial data in various ways, such as zooming, panning, and selecting features to find information.
* manipulate layers by adding or turning them on or off for display, or change their symbology on the screen.
* perform spatial analysis, such as measuring distances between features or calculating areas, and conduct spatial overlay analysis or compare different datasets and identify patterns and trends in the data.
* generate reports and create spatial information products from displayed data.
* create visualizations of spatial data in various formats, including maps, charts, and tables, and share and communicate them with others.

**2.1.2. The GIS BB MUST enable GIS Data Editors to**

* add new features to a dataset (e.g. add a new building to a map of a city).
* delete features from a dataset (e.g. delete the location of a wrongly reported accident from a map).
* update the attributes of features in a dataset (e.g. update the address of a building).
* modify features (e.g. correct the river stream on a map).
* merge/combine two or more datasets into a single dataset (e.g. merge a dataset of water bodies with a dataset of forests to create a single dataset of land cover).
* divide a dataset into two or more datasets (e.g. split a dataset of buildings into two datasets, one for residential buildings and one for commercial buildings).
* check the accuracy and completeness of a dataset (e.g. ensure that the roads in a layer are intersecting properly).
* export a dataset to a file for use in other software applications.

**2.1.3. The GIS BB MUST enable GIS Data Admin to**

* migrate data from one database to another.
* create new layers, delete existing layers, and manage the properties of layers of standard GIS/CAD/Raster data formats.
* connect to remote databases and access data from those databases.
* import data from external sources and export data to external sources.
* search for data by name, type, path, or keyword tag.
* transform and convert the projections and georeferenced coordinate systems to common formats.
* generate metadata automatically or manually.
* import and export metadata.
* enforce metadata standards.
* change and enforce data manipulation policies and integrity constraints.
* track changes to data and metadata.

**2.1.4. The GIS BB MUST enable GIS Developer to**

* expose capabilities to access GIS databases, GIS layers, and associated attributes.
* provide access to the contents of databases for data query, extraction, and replication.
* provide access to the contents of a map, such as the layers and their underlying attributes.
* develop interoperable applications for the exchange of data and services between different systems that integrate, consume, and/or share geospatial data and services compliant with common standards such as the OGC and ISO 191xx series.
* create mobile apps that can be used to collect and analyze geospatial data.
* integrate and communicate with other GIS applications and GIS data sources, such as social media data or weather data.

**2.1.5. The GIS BB MUST enable Discovery Services to**

* catalog geospatial data by providing information about the data, such as its location, format, and metadata.
* search for geospatial data by using keywords, tags, or other criteria.
* visualize geospatial data by displaying it on a map or other visualization.
* provide access to geospatial data by allowing users to download it, use it in their application, or generate a report.

**2.1.6. The GIS BB MUST enable Other Building Blocks and application to**

* retrieve geospatial data used to create interactive maps, geovisualizations, and applications.
* perform geospatial analysis to make spatially-informed decisions or gain spatial insights (e.g., finding the closest point of interest, calculating the area of a polygon, or identifying the route between two points).
* manage geospatial data, such as creating, editing, and deleting features in a variety of formats, such as Shapefiles, GeoJSON, and KML.

## 2.2 Out of Scope

The following aspects are out of the scope of the current version of the GIS Building Block specifications considered in this document:

* Processing of raster data (e.g., satellite and drone imagery, gridded data) such as performing image classification, image enhancement, segmentation, and other types of analysis.
* Performing complex geospatial analysis, such as spatial interpolation or complex spatial statistics (e.g., spatial autocorrelation and spatial regression)
* Handling and performing analysis of geometric networks (typically associated with rules-based networks such as water distribution lines, power utilities, electrical lines, gas pipelines, telephone services, and stream/river water flows).
* Sharing and accessing GIS 3D data models such as TINs, BLMs, and scenery.
* Analysis of 3D GIS data models such as performing LiDAR analysis, volumetric calculations, or 3D modeling.
* Supporting time-based dynamic tracking of objects, whether those that are GPS/sensor-based such as Automatic Vehicle Location (AVL) or spatiotemporal based on time-stamped such as traffic accidents or weather storms.
* Adapting to or addressing a country's specific data privacy policies and any legal or ethical implications associated with the amount and level of information that GIS BB services can gather. It is important to carefully consider any legal or ethical implications associated with using the GIS BB services according to the context and applications they serve, and to take measures to ensure that any collected data is being used responsibly and appropriately.

