# Spanish Cadastral Properties Ontology

This ontology allows representing the domain of the Spanish Real Estate Cadastre, focused on cadastral parcels, cadastral properties and cadastral constructions.

It is being developed in the context of the Data Space for Smart Urban Infrastructures ([EDINT](https://edint.es/)).

# Ontology purpose and scope

The purpose of this ontology is to model the fundamental entities and relationships of the Spanish Real Estate Cadastre to enable interoperability of cadastral data in the context of Linked Data. The scope is limited to cadastral parcels, cadastral properties, cadastral constructions, cadastral references, addresses, uses and classifications, and geometries and areas. Aspects such as property ownership, cadastral valuation, transfer data and administrative processes are out of scope.

# Prefix and namespace

The prefix of this ontology is `edintcat`. It is published in the namespace: http://vocab.linkeddata.es/datosabiertos/def/catastro/

# Ontology Conceptualization

![Conceptual model diagram](diagrams/diagrama-catastro.drawio.png)

# Repository structure

The repository contains the following folders:

| Folder | Description |
|--------|--------------|
| **diagrams/** | Stores diagrams and other resources representing the conceptual model of the ontology (e.g., class hierarchies, relationships). |
| **documentation/** | Stores the HTML or human oriented documentation of the ontology and related artefacts. |
| **examples/** | Includes examples that demonstrate how to instantiate or apply the ontology in real data scenarios. |
| **kos/** | Stores controlled vocabularies or KOS implementation, usually SKOS implementations in rdf. |
| **ontology/** | Contains the actual ontology implementation files in formats such as `.owl`, `.rdf`, `.ttl`, or `.jsonld`. |
| **requirements/** | Contains all documents used to define the ontology's requirements: data example, competency questions, functional requirements, use cases, etc. |
| **shapes/** | Contains the SHACL shapes used to define and validate ontology constraints. |
| **tests/** | Stores tests for ontology evaluation. |

# Maintenance and evolution

To manage those incidents or suggested improvements with respect to the vocabulary, we recommend you to follow
the guides provided in [Issues Management](./ISSUES.md) to
generate an issue.

# Funding

This ontology has been developed in the context of the Data Space for Smart Urban Infrastructures ([EDINT](https://edint.es/)).

![Logos](./resources/EDINT_UE_V-Color.png)
