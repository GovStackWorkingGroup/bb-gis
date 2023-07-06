---
description: This section provides context for this Building Block.
---

# 2 Description

Geospatial information represents Earth's features, including maps, images, addresses, zip codes, phone numbers, landmarks, events, and more. Location and time are fundamental properties of geographic information, providing a unifying theme to understand the context of most real and abstract phenomena.

The GIS (geographic information services) building block enables various applications with location-based capabilities. By integrating a wide range of spatial data, such as maps, imagery, and location-based services, users can access and process geospatial data from different sources and link geographic locations to various "objects" within an open information technology environment. For example, users can link geographic locations to people, such as patients, doctors, farmers, and agricultural extension practitioners. They can also link geographic locations to hospitals, ambulances, labs, seed production facilities, and more. Additionally, equipment such as ventilators and vaccine containers can be linked to geographic locations, as can sites like water sources and agricultural fields. This geographic association can also be tagged with a unique digital identifier and a timestamp of when it was acquired.

Applications or components using geographical information services can collect, share, and use temporal and spatial information with other applications, such as map repositories and data visualization tools. These tools can display the collected information on geographical maps, giving users a powerful visual representation of the data. Furthermore, the collected data can be combined with other datasets, such as population, surveillance, or supply chain datasets, to enable interoperable geospatial and spatiotemporal analysis. This can help identify patterns and trends in the data that might not otherwise be apparent.

## 2.1 **Relation to Existing Geospatial Information Standards**

The GovStack GIS BB specifications are not meant to replace or compete with existing standards in GIS but rather to extend them to address a new niche related to application use cases serving specific sectors. There are several initiatives and entities dedicated to creating standards for geographic data, the most popular of which are: (1) ISO Technical Committee 211 on Geographic Information/Geomatics (ISO/TC 211) which produces the ISO 19xxx standard series, and (2) the Open Geospatial Consortium (OGC). Although these two organizations are independent and sometimes produce overlapping standards, they generally coordinate closely to maximize mutual development and minimize duplication.

ISO standards are generally focused on the nature of geographic information and standards to encode and represent it in digital environments, while OGC standards are more focused on implementation of services and APIs for serving and processing GIS over the internet or across systems.

The GovStack GIS BB specifications were developed to fill a new niche in the GIS standardization landscape. Instead of dealing with each standard in isolation or representing them abstractly, these specifications focus on converging existing standards and aligning them in a useful and applicable way to real-world scenarios or use cases relevant to governments and municipalities.

&#x20;

<figure><img src=".gitbook/assets/image (1).png" alt="" width="375"><figcaption><p>Relation to main standards in the Geospatial Information Domain</p></figcaption></figure>

Specifically, the GovStack GIS BB specifications aim to:

* **Make it easier for governments to adopt and use open standards for GIS.**
* **Help governments build more interoperable and reusable GIS applications and integrate them with other building blocks.**
* **Enable governments to deliver more efficient and effective geo-enabled services to citizens and businesses.**

By extending existing standards and focusing on application use cases, the GovStack GIS BB specifications can help governments realize the full potential of GIS to improve public services and decision-making. Below are a few examples of the many sectors that can benefit from GIS services and applications.

* **Local government:** cadastral mapping and management, land use and transportation planning, and optimization of service delivery such as postal services, trash collection, etc.
* **Incident Management and Emergency Response**: call services, dispatching, tracking emergency vehicles and resources, redlining, etc.
* **Law enforcement:** tracking crime patterns, investigating crimes, and public safety planning
* **Natural resources:** managing water resources, monitoring forests, and conservation planning
* **Planning:** planning for development, transportation, and other infrastructure projects
* **Agriculture:** tracking crop yields, providing weather information for farmers, planning for agricultural development, and precision farming
* **Business:** tracking assets and customer shopping habits, analyzing store locations, and supply chain management
* **Construction:** planning construction projects, tracking progress, and identifying potential hazards
* **Energy:** management of energy resources, planning for green energy development, and monitoring energy use
* **Environment:** measuring pollution, monitoring wildlife populations, and environmental protection
* **Healthcare:** managing disease outbreaks, planning for healthcare facilities, and improving access to patient care
* **Risk management:** modeling hazards, exposure, vulnerability analysis, and risk assessment and management
* **Transportation:** planning transportation routes, tracking traffic, and improving public transportation
* **Utilities:** utility infrastructure management, customer data management, and utility expansion planning

## 2.2 **Current scope**

The functional requirements to cover the services required from the GIS Building Block currently consider the specific use cases of:

* GIS-Based Incident Management System ([https://govstack-global.atlassian.net/l/cp/jPn05EbR](https://govstack-global.atlassian.net/l/cp/jPn05EbR))
* Land Records/Cadastre Management ([https://govstack-global.atlassian.net/l/cp/0dcEf3cm](https://govstack-global.atlassian.net/l/cp/0dcEf3cm))

These two use cases cover a wide range of GIS services, including core functionality such as GIS data access, display, and visualization, GIS data query, GIS layer management and manipulation, metadata and cataloging services, locational analysis, geocoding, and reporting. The endless combination of these GIS services can be used to respond to the needs of various applications across many domains and sectors, as listed above.

The following actors have been identified as "users" of the GIS Building Block:

* "**GIS Data Viewer**": displays and views spatial data to find information about a particular location, compare different datasets, or create spatial data visualizations.
* "**GIS Data Editor**": performs spatial data editing by adding, updating, or deleting geographic data features from a dataset or changing the properties and attributes of these features.
* "**GIS Admin**": manages GIS data by creating, maintaining, and organizing geographic datasets and ensuring that data is accurate and up-to-date.
* "**GIS Application Developer**": develops GIS applications by deploying one or more GIS BB services to serve business needs.
* "**Discovery Tools**": search for metadata about spatial data to find information about the content of a dataset, the creators of a dataset, or the methods used to create a dataset.
* "**Other Building Blocks and Applications**": display and consume GIS services to perform specific GIS operations such as creating maps, generating reports, and more.

The GIS BB services MUST enable these actors to perform the basic functions and tasks associated with their role as follows:

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

## 2.3 Future Scope

The following aspects are on the future scope for the GIS Building Block specifications considered in this document:

* Processing of raster data (e.g., satellite and drone imagery, gridded data) such as performing image classification, image enhancement, segmentation, and other types of analysis.
* Performing complex geospatial analysis, such as spatial interpolation or complex spatial statistics (e.g., spatial autocorrelation and spatial regression)
* Handling and performing analysis of geometric networks (typically associated with rules-based networks such as water distribution lines, power utilities, electrical lines, gas pipelines, telephone services, and stream/river water flows).
* Sharing and accessing GIS 3D data models such as TINs, BLMs, and scenery.
* Analysis of 3D GIS data models such as performing LiDAR analysis, volumetric calculations, or 3D modeling.
* Supporting time-based dynamic tracking of objects, whether those that are GPS/sensor-based such as Automatic Vehicle Location (AVL) or spatiotemporal based on time-stamped such as traffic accidents or weather storms.

## 2.4 Out of Scope

The following aspects are out of the scope of the current version of the GIS Building Block specifications considered in this document:

* The GIS BB specifications do not address a country's specific data privacy policies, as well as any legal or ethical implications associated with the amount and level of information that can be gathered by GIS BB services. It is crucial to carefully consider any legal or ethical implications associated with using these tools and to take steps to ensure that any collected data is being used responsibly and appropriately.
* The GIS BB specifications do not define the security measures that should be used to protect GIS data. Security requirements for geographic data can vary depending on the sensitivity of the data and the environment in which it is used.
* The GIS BB specifications do not define the data formats that should be used to store or exchange geographic data. Many different data formats are available, each with its advantages and disadvantages.
* The GIS BB specifications do not define the quality of the geographic data that should be used. The quality of geographic data can vary depending on the source of the data and the methods used to collect it.
*   The GIS BB specifications do not define how geographic data should be visualized. This is because geographic data visualization is a subjective process that depends on the user’s needs.

    .
