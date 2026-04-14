# Ontología EDINT del Catastro Español (EDINT Spanish Cadastre Ontology)

La ontología del Catastro Español representa el dominio del Catastro Inmobiliario Español, centrada en tres entidades principales: parcelas catastrales, inmuebles catastrales y construcciones catastrales.

The Spanish Cadastre Ontology represents the domain of the Spanish Real Estate Cadastre, focused on three main entities: cadastral parcels, cadastral properties, and cadastral constructions.

# Propósito y alcance de la ontología (Purpose and scope of the ontology)

El propósito de la ontología del Catastro Español es modelar las entidades y relaciones fundamentales del Catastro Inmobiliario Español para habilitar la interoperabilidad de datos catastrales en el contexto de los datos enlazados (Linked Data).

The purpose of the Spanish Cadastre Ontology is to model the fundamental entities and relationships of the Spanish Real Estate Cadastre to enable interoperability of cadastral data in the context of Linked Data.

El alcance de la ontología está limitado a:

The scope of the ontology is limited to:

- **Parcelas Catastrales** (Cadastral Parcels) - Unidades básicas de división territorial
- **Inmuebles Catastrales** (Cadastral Properties) - Bienes inmobiliarios (viviendas, locales) con independencia de uso
- **Construcciones Catastrales** (Cadastral Constructions) - Unidades constructivas dentro de inmuebles
- **Referencias Catastrales** (Cadastral References) - Identificadores únicos de parcelas e inmuebles
- **Direcciones** (Addresses) - Ubicación geográfica mediante el vocabulario Callejero
- **Usos y Clasificaciones** (Uses and Classes) - Clasificación según vocabularios KOS de EDINT
- **Geometrías y Áreas** (Geometries and Areas) - Información espacial con GeoSPARQL

- **Cadastral Parcels** - Basic territorial division units
- **Cadastral Properties** - Real estate properties (dwellings, premises) with independent use
- **Cadastral Constructions** - Construction units within properties
- **Cadastral References** - Unique identifiers for parcels and properties
- **Addresses** - Geographic location using the Callejero vocabulary
- **Uses and Classifications** - Classification according to EDINT KOS vocabularies
- **Geometries and Areas** - Spatial information with GeoSPARQL

La ontología **NO** cubre:

The ontology **DOES NOT** cover:

- Titularidad de bienes (ownership, registry data)
- Valoración catastral (valuation, tax values)
- Datos de transmisiones (sales, transfers)
- Procesos administrativos (registration procedures)

- Titularidad de bienes (ownership, registry data)
- Valoración catastral (valuation, tax values)
- Datos de transmisiones (sales, transfers)
- Procesos administrativos (registration procedures)

# Prefijo y espacio de nombres (Prefix and namespace)

El prefijo de la ontología es: `edintcat` y se encuentra publicada en el espacio de nombres: [http://vocab.linkeddata.es/datosabiertos/def/catastro/](http://vocab.linkeddata.es/datosabiertos/def/catastro/)

The prefix of the ontología is: `edintcat` and is published in the namespace: [http://vocab.linkeddata.es/datosabiertos/def/catastro/](http://vocab.linkeddata.es/datosabiertos/def/catastro/)

Versión actual: 0.1.0

Current version: 0.1.0

# Modelo conceptual (Ontology conceptualization)

![Diagrama del modelo conceptual del Catastro](diagrams/diagrama-catastro.drawio.png)

![Cadastral ontology conceptual model diagram](diagrams/diagrama-catastro.drawio.png)

El diagrama muestra las tres entidades principales y sus relaciones:

The diagram shows the three main entities and their relationships:

- **CadastralParcel** → **CadastralProperty** (una parcela contiene uno o más inmuebles)
- **CadastralProperty** → **CadastralConstruction** (un inmueble tiene una o más construcciones)
- Integración con vocabularios externos:
  - **GeoSPARQL**: Para geometrías (WKT) y medidas de área (m²)
  - **Callejero**: Para direcciones (calle, número, código postal, municipio, provincia)
  - **KOS de EDINT**: Para usos (Residencial, Comercial, etc.) y clases (Urbano, Rústico)

- **CadastralParcel** → **CadastralProperty** (a parcel contains one or more properties)
- **CadastralProperty** → **CadastralConstruction** (a property has one or more constructions)
- Integration with external vocabularies:
  - **GeoSPARQL**: For geometries (WKT) and area measurements (m²)
  - **Callejero**: For addresses (street, number, postal code, municipality, province)
  - **EDINT KOS**: For uses (Residential, Commercial, etc.) and classes (Urban, Rural)

# Estructura del repositorio (Repository structure)

El repositorio contiene (al menos) las siguientes carpetas:

The repository contains (at least) the following folders:

| Carpeta | Descripción |
|--------|--------------|
| **diagrams/** | Contiene diagramas y otros recursos que representan el modelo conceptual de la ontología (por ejemplo, jerarquías de clases, relaciones). |
| **documentation/** | Contiene la documentación de la ontología y artefactos relacionados en formato HTML o dirigida a usuarios. |
| **tests/** | Contiene las pruebas para la evaluación de la ontología. |
| **kos/** | Contiene la implementación de vocabularios controlados o KOS, generalmente implementaciones SKOS en RDF.|
| **ontology/** | Contiene los archivos de implementación de la ontología en formatos como .owl, .rdf, .ttl o .jsonld |
| **requirements/** | Contiene todos los documentos utilizados para definir los requisitos de la ontología: ejemplos de datos, preguntas de competencia, requisitos funcionales, casos de uso, etc. |
| **shapes/** | Contiene las restricciones SHACL utilizad para validar datos respecto a la ontología.  |
| **examples/** | Contiene ejemplos de instancias de la ontología que ilustran su uso práctico. |

| Folder | Description |
|--------|--------------|
| **diagrams/** | Contains diagrams and other resources representing the conceptual model of the ontology (e.g., class hierarchies, relationships). |
| **documentation/** | Contains ontology documentation and related artifacts in HTML format or aimed at users. |
| **tests/** | Contains tests for ontology evaluation. |
| **kos/** | Contains the implementation of controlled vocabularies or KOS, generally SKOS implementations in RDF.|
| **ontology/** | Contains ontology implementation files in formats such as .owl, .rdf, .ttl or .jsonld |
| **requirements/** | Contains all documents used to define ontology requirements: data examples, competency questions, functional requirements, use cases, etc. |
| **shapes/** | Contains SHACL constraints used to validate data against the ontology.  |
| **examples/** | Contains example ontology instances that illustrate practical usage. |

# Clases principales (Main Classes)

La ontología define las siguientes clases principales:

The ontology defines the following main classes:

| Clase | Descripción |
|---------|-------------|
| **CadastralParcel** | Unidad básica de división territorial. Representa una porción de terreno delimitada geográficamente. |
| **CadastralProperty** | Bien inmueble inscrito en el Catastro. Puede ser una vivienda, local, o cualquier unidad de uso independiente. |
| **CadastralReference** | Referencia catastral completa compuesta por referencia de parcela y referencia de inmueble. |
| **CadastralConstruction** | Edificio o construcción registrada sobre un inmueble catastral. Incluye datos de área, uso, y características constructivas. |
| **Renovation** | Evento o proceso de reforma de una construcción, incluyendo información sobre cuándo ocurrió y qué tipo de reforma se realizó. |

| Class | Description |
|---------|-------------|
| **CadastralParcel** | Basic unit of territorial division. Represents a geographically delimited portion of land. |
| **CadastralProperty** | Real estate property registered in Cadastre. Can be a dwelling, premises, or any independent use unit. |
| **CadastralReference** | Complete cadastral reference composed of parcel reference and property reference. |
| **CadastralConstruction** | Building or construction registered on a cadastral property. Includes area, use, and construction characteristics data. |
| **Renovation** | Event or process of renovation of a construction, including information about when it occurred and what type of renovation was performed. |

# Propiedades principales (Main Properties)

| Propiedad | Tipo | Descripción |
|------------|-------|-------------|
| **hasCadastralProperty** | Object | Relación Parcela → Inmueble |
| **onCadastralParcel** | Object | Relación Inmueble → Parcela (inversa) |
| **hasCadastralConstruction** | Object | Relación Inmueble → Construcción |
| **onCadastralProperty** | Object | Relación Construcción → Inmueble (inversa) |
| **hasCadastralReference** | Object | Vincula entidad con su referencia catastral |
| **hasAddress** | Object | Vincula inmueble o parcela con dirección (vocabulario Callejero) |
| **hasUse** | Object | Asigna uso principal (vocabulario KOS) |
| **hasClass** | Object | Asigna clasificación urbana/rural (vocabulario KOS) |
| **participation** | Datatype | Porcentaje de participación en elementos comunes (%) |
| **supportPercentage** | Datatype | Porcentaje de área considerada soporte (%) |
| **constructionYear** | Datatype | Año de construcción (gYear) |
| **staircase** | Datatype | Identificador de escalera |
| **floor** | Datatype | Planta (puede ser negativa para sótanos) |
| **door** | Datatype | Puerta o número de unidad |

| Property | Type | Description |
|------------|-------|-------------|
| **hasCadastralProperty** | Object | Parcel → Property relationship |
| **onCadastralParcel** | Object | Property → Parcel relationship (inverse) |
| **hasCadastralConstruction** | Object | Property → Construction relationship |
| **onCadastralProperty** | Object | Construction → Property relationship (inverse) |
| **hasCadastralReference** | Object | Links entity with its cadastral reference |
| **hasAddress** | Object | Links property or parcel with address (Callejero vocabulary) |
| **hasUse** | Object | Assigns main use (KOS vocabulary) |
| **hasClass** | Object | Assigns urban/rural classification (KOS vocabulary) |
| **participation** | Datatype | Participation percentage in common elements (%) |
| **supportPercentage** | Datatype | Percentage of area considered support (%) |
| **constructionYear** | Datatype | Construction year (gYear) |
| **staircase** | Datatype | Staircase identifier |
| **floor** | Datatype | Floor (can be negative for basements) |
| **door** | Datatype | Door or unit number |

# Vocabularios utilizados (Used Vocabularies)

La ontología reutiliza los siguientes vocabularios estándar:

The ontology reuses the following standard vocabularies:

- **GeoSPARQL** (`http://www.opengis.net/ont/geosparql#`) - Para geometrías espaciales y medidas
- **Callejero** (`http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/callejero#`) - Para direcciones españolas
- **SKOS** (`http://www.w3.org/2004/02/skos/core#`) - Para vocabularios controlados
- **QUDT** (`http://qudt.org/schema/qudt/`) - Para unidades de medida (m², %)
- **KOS de EDINT**:
  - **Usos** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/`) - Clasificación de usos catastrales (RD 1020/1993)
  - **Clases** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/`) - Clasificación urbana/rural (RDLeg 1/2004)

- **GeoSPARQL** (`http://www.opengis.net/ont/geosparql#`) - For spatial geometries and measurements
- **Callejero** (`http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/callejero#`) - For Spanish addresses
- **SKOS** (`http://www.w3.org/2004/02/skos/core#`) - For controlled vocabularies
- **QUDT** (`http://qudt.org/schema/qudt/`) - For measurement units (m², %)
- **EDINT KOS**:
  - **Uses** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/`) - Cadastral use classification (RD 1020/1993)
  - **Classes** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/`) - Urban/rural classification (RDLeg 1/2004)

# Cómo usar esta ontología (How to use this ontology)

## Ejemplos de uso (Usage Examples)

Consulte la carpeta `examples/` para ver ejemplos completos de instancias de la ontología:

See the `examples/` folder for complete examples of ontology instances:

- **cadastral-parcel-complete-example.ttl** - Ejemplo completo de una parcela con 98 construcciones
- **examples/README.md** - Documentación detallada de los ejemplos

- **cadastral-parcel-complete-example.ttl** - Complete example of a parcel with 98 constructions
- **examples/README.md** - Detailed documentation of the examples

## Consultas SPARQL (SPARQL Queries)

La carpeta `requirements/` contiene consultas SPARQL que responden a preguntas de competencia del dominio catastral:

The `requirements/` folder contains SPARQL queries that answer competency questions of the cadastral domain:

- **requirements/requirements.csv** - Preguntas de competencia y su mapeo a elementos de la ontología
- **requirements/CAT*.sparql** - Consultas SPARQL para cada pregunta de competencia (CAT01-CAT18)

- **requirements/requirements.csv** - Competency questions and their mapping to ontology elements
- **requirements/CAT*.sparql** - SPARQL queries for each competency question (CAT01-CAT18)

Ejemplo de consulta para obtener todas las parcelas catastrales:

Example query to get all cadastral parcels:

```sparql
PREFIX edintcat: <https://edint.github.io/edint-ontologia-inmuebles/ontology/catastro#>

SELECT ?parcel ?parcelRef ?propertyRef WHERE {
    ?parcel a edintcat:CadastralParcel ;
            edintcat:hasCadastralReference ?ref .

    ?ref a edintcat:CadastralReference ;
         edintcat:parcelReference ?parcelRef ;
         edintcat:propertyReference ?propertyRef .
}
```

## Validación (Validation)

Para validar datos o la ontología, utilice el script de validación:

To validate data or the ontology, use the validation script:

```bash
python tests/validate.py ontology/catastro.ttl
python tests/validate.py examples/*.ttl
```

Este script verifica sintaxis RDF, consistencia de tipos, y uso correcto de propiedades.

This script checks RDF syntax, type consistency, and correct property usage.

# Mantenimiento y evolución (Maintenance and evolution)

Para manejar las incidencias o mejoras sugeridas con respecto a la ontología, recomendamos seguir las guías proporcionadas en ([Issues Management](./ISSUES.md)) para generar una incidencia.

For managing issues or suggested improvements regarding the ontology, we recommend following the guidelines provided in ([Issues Management](./ISSUES.md)) to create an issue.

# Versión y licencia (Version and License)

[![Version: 0.1.0](https://img.shields.io/badge/Version-0.1.0-blue)](https://github.com/edint/edint-ontologia-catastro)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

Esta ontología ha sido desarrollada en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es)).

This ontology has been developed in the context of the Data Space for Smart Urban Infrastructures ([EDINT](https://edint.es)).

# Financiación (Funding)

Esta ontología ha sido desarrollada en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es)).

This ontology has been developed in the context of the Data Space for Smart Urban Infrastructures ([EDINT](https://edint.es)).

![Logos](./resources/EDINT_UE_V-Color.png)
