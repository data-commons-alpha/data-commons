---
title: "Entity Relationship Diagram"
keywords: documentation
tags: [documentation]
sidebar: admin_sidebar
permalink: erd.html
summary: Data model for the Serves' Service Episodes
---

## Data model
![data model](/data-commons/images/erd.png)

* The core entity of this model is the Service Episode Entity (se_episode). Its relationship to other entities (i.e. Network - se_network) is enforced through the unique mapping of the service_episode_id attribute.  
### Service Episode - Network Relationship
* The service episode entity can be worked on my many network entities, and a network entity can be part of many service episodes; thus, a many-to-many relationship exists, and an associative entity (se_network_episode) is required to track the unique service episode to network mapping.
![](/data-commons/images/epi_net_MM.png)
### Network - Organization Relationship
* The many-to-many construct described above also applies to network and organization entities, therefore, another associative entity (se_network_organization) is required.
![](/data-commons/images/net_org_MM.png)
