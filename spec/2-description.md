---
description: This section provides context for this Building Block.
---

# 2 Description

Geospatial information represents Earth's features, including maps, images, addresses, zip codes, phone numbers, landmarks, events, and more. Location and time are fundamental properties of geographic information, providing a unifying theme to understand the context of most real and abstract phenomena.

The GIS (geographic information services) building block enables various applications with location-based capabilities. By integrating a wide range of spatial data, such as maps, imagery, and location-based services, users can access and process geospatial data from different sources and link geographic locations to various "objects" within an open information technology environment. For example, users can link geographic locations to people, such as patients, doctors, farmers, and agricultural extension practitioners. They can also link geographic locations to hospitals, ambulances, labs, seed production facilities, and more. Additionally, equipment such as ventilators and vaccine containers can be linked to geographic locations, as can sites like water sources and agricultural fields. This geographic association can also be tagged with a unique digital identifier and a timestamp of when it was acquired.

Applications or components using geographical information services can collect, share, and use temporal and spatial information with other applications, such as map repositories and data visualization tools. These tools can display the collected information on geographical maps, giving users a powerful visual representation of the data. Furthermore, the collected data can be combined with other datasets, such as population, surveillance, or supply chain datasets, to enable interoperable geospatial and spatiotemporal analysis. This can help identify patterns and trends in the data that might not otherwise be apparent.

## 2.1 **Relation to Existing Geospatial Information Standards**

The GovStack GIS BB specifications are not meant to replace or compete with existing standards in GIS but rather to extend them to address a new niche related to application use cases serving specific sectors. There are several initiatives and entities dedicated to creating standards for geographic data, the most popular of which are: (1) ISO Technical Committee 211 on Geographic Information/Geomatics (ISO/TC 211) which produces the ISO 19xxx standard series, and (2) the Open Geospatial Consortium (OGC). Although these two organizations are independent and sometimes produce overlapping standards, they generally coordinate closely to maximize mutual development and minimize duplication.

ISO standards are generally focused on the nature of geographic information and standards to encode and represent it in digital environments, while OGC standards are more focused on the implementation of services and APIs for serving and processing GIS over the internet or across systems. Links to the respective standards and resources that are incorporated in the GIS BB can be found in section 5.5 of the GIS BB specifications.

The GovStack GIS BB specifications were developed to fill a new niche in the GIS standardization landscape. Instead of dealing with each standard in isolation or representing them abstractly, these specifications focus on converging existing standards and aligning them in a useful and applicable way to real-world scenarios or use cases relevant to governments and municipalities.

<figure><img src=".gitbook/assets/image (7).png" alt="" width="375"><figcaption><p>Relation to main standards in the Geospatial Information Domain</p></figcaption></figure>

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

* **Enable GIS Data Viewers to** explore, and analyze spatial data, interact with various types of spatial data, manipulate layers, perform spatial analysis, generate reports and create spatial information products, create visualizations in different formats, and share them with others.
* **Provide capabilities for GIS Data Editors** to add, delete, update, and modify features in a dataset. It should also support merging or dividing datasets, checking accuracy and completeness, and exporting datasets for use in other software applications.
* **Enable GIS Data Admin** to migrate data between databases, create and manage layers, connect to remote databases, import/export data from external sources, search for data, transform projections, generate and manage metadata, enforce metadata standards, enforce data manipulation policies and integrity constraints, and track changes to data and metadata.
* **Allow GIS Developers** to expose capabilities for accessing GIS databases, provide access to database contents, access map contents, develop interoperable applications, create mobile apps for geospatial data, and integrate and communicate with other GIS applications and data sources.
* **Enable Discovery Services** to catalog, search, visualize, and provide access to geospatial data by providing information about the data, using keywords or tags, displaying it on a map, and allowing users to download, use, or generate reports.
* **Allow other building blocks and applications** to retrieve geospatial data for creating interactive maps and applications, perform geospatial analysis for spatially-informed decisions, and manage geospatial data in various formats.

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
