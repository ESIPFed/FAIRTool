# FAIRTool.org


# Overview

FAIRTool is a semantic web application to provide stewardship to Earth science research output. The tool will implement the 15 FAIR principles. The core of FAIRTool is the FAIR-O Ontology which will be built following these 15 FAIR principles. The web application will use FAIR-O Ontology to capture the properities equivilant to the 15 FAIR principle and display them as metadata. Through a technical pipeline, a score for each principle will be calculated and displayed as the FAIRness score of that research output. The created metadata record from the FAIRTool can be downloaded as RDF file. The FAIRTool can be used by both researchers and data managers, as well as other users.

FAIRTool (FAIRTool.org) is a framework that provides metadata conforms to FAIR principles. FAIRTool uses a composition of well-known ontologies (e.g. Schema.org, DCAT, PROV, FOAF, VOID, SKOS, VCARD, ODRL), semantic web technologies, web application, and a database for creating, storing and serving FAIR metadata of research output.

FAIRtool.org is a semantic web application that allows data creators to describe a dataset with FAIR metadata and, in the other side, allows data users to discover information (metadata) about the offered datasets and, if the data is open access, the actual data can be retrieved.

The FAIRTool application is being initially developed as a stand-alone web application. However, the SPARQL endpoint of the FAIRTool can be also accessed from other applications to provide FAIR metadata accessibility of the datasets. 



# Timeline

  - Feb.- Mar., 2019 Project plan report; Architecture design; Ontologies bulding, Application creation and integration.
  - Apr.- Jun., 2019 Write program codes; Triple store setup;  development.
  - Jul., 2019 Online testing, debugging and implementation of deliverables; 
  - Jul. 18, 2019 Presenting FAIRtool.org at ESIP 2019 summer meeting.
  - Aug., 2019 Project final report writing.
  - Sep. - Oct. 2019 FAIRtool.org online Beta release, accepting access requests for usernames to ESIP community
  - Nov. - Dec. 2019 Aplication tune up and final release.  
  - Jan. - 2020 present the Earth science scientific dataset's metadata case study output at ESIP 2020 winter meeting.


FAIRTool main components: 

- As a database, it holds and relates information on research output artifacts (e.g., data and software, and more),  
- As a web application, it provides intelligence and reporting on Earth Science community research output artifacts. 
- Through its integration to other registration systems (e.g., DOI, ORCID, CC, etc.), via APIs it produces essential information vital to FAIR metadata system.  
- Through its API and SPARQL endpoint, it supports data mining for special purpose and ad hoc needs.  
- Through linked data, it is one of the Earth science community face to the Web of Data. 
- With small update, it can also be applied to data in other disciplines. 


Proposed FAIRTool Architecture: 

- Data Pipeline fetched from multiple known sources via APIs, then loads into the FAIR triple datastore. 
- FAIR-O Ontology describes the FAIR classes and the relation between classes to form a FAIR metadata of the Earth Science community research output.  
- FAIR Triple Datastore allows storing, indexing, and hold complex relationship between entities as well as real-time  population of downstream datastores (e.g., representations for web app usage); 
- GUI Web Application exposes FAIR metadata reports, & landing pages for FAIRTool entities sufficient to satisfy the 15 FAIR principles requirements combined with FAIRness score.

Tech Selections: 

- Data Pipeline: Integration APIs provided from DataCite, ORCID, Creative Commons, and others. 
- Triple Datastore: Vitro with Jena and OpenLink’s virtuoso. 
https://vivoweb.org/info/about-vitro   
- Web App/GUI: Java scripts, and Freemarker. 
- Web Server: Apache Tomcat 
