# Ejemplos de la Ontología del Catastro Español (Examples of Spanish Cadastre Ontology)

Esta carpeta contiene ejemplos de instancias de la ontología del Catastro Español que ilustran cómo modelar diferentes entidades catastrales utilizando Turtle (.ttl).

This folder contains example instances of the Spanish Cadastre Ontology that illustrate how to model different cadastral entities using Turtle (.ttl).

# Propósito (Purpose)

El objetivo de estos ejemplos es demostrar el uso práctico de la ontología del Catastro Español para modelar:

- **Parcelas Catastrales** (Cadastral Parcels) - Unidades básicas de división territorial
- **Inmuebles Catastrales** (Cadastral Properties) - Unidades de uso independientes (viviendas, locales)
- **Construcciones Catastrales** (Cadastral Constructions) - Unidades constructivas dentro de inmuebles
- **Referencias Catastrales** (Cadastral References) - Identificadores únicos de parcelas e inmuebles
- **Direcciones** (Addresses) - Ubicación mediante vocabulario callejero
- **Geometrías y Áreas** (Geometries and Areas) - Información espacial con GeoSPARQL
- **Usos y Clasificaciones** (Uses and Classes) - Uso del vocabulario KOS de EDINT

The purpose of these examples is to demonstrate the practical use of the Spanish Cadastre Ontology to model:

- **Parcelas Catastrales** (Cadastral Parcels) - Basic territorial division units
- **Inmuebles Catastrales** (Cadastral Properties) - Independent use units (dwellings, premises)
- **Construcciones Catastrales** (Cadastral Constructions) - Construction units within properties
- **Referencias Catastrales** (Cadastral References) - Unique identifiers for parcels and properties
- **Direcciones** (Addresses) - Location using the callejero vocabulary
- **Geometrías y Áreas** (Geometries and Areas) - Spatial information with GeoSPARQL
- **Usos y Clasificaciones** (Uses and Classes) - Usage of EDINT KOS vocabulary

# Formatos Aceptados (Accepted Formats)

Los ejemplos se proporcionan en los siguientes formatos:

- **`.ttl`** - Serialización en Turtle (Turtle Notation), formato recomendado para Linked Data
- **`.pdf`** - Documentos de referencia del Catastro Español (fuentes oficiales)

The examples are provided in the following formats:

- **`.ttl`** - Turtle serialization, recommended format for Linked Data
- **`.pdf`** - Reference documents from the Spanish Cadastre (official sources)

# Ejemplos Disponibles (Available Examples)

## 1. `cadastral-parcel-complete-example.ttl`

Este ejemplo completo muestra una parcela catastral con toda su información:

- **Parcela catastral**: `Parcela_8942103VK2793`
  - Referencia catastral: `8942103VK2793`
  - Clasificación: Urbano
  - Geometría WKT y área (407.586 m²)
  - Dirección: Calle Badajoz 348[B], 28223 Pozuelo de Alarcón, Madrid

- **Inmueble catastral**: `Inmueble_8942103VK2793S0001UO`
  - Referencia catastral: `8942103VK2793S0001UO`
  - Participación: 100.00%
  - Uso: Cultural
  - Clasificación: Urbano
  - Dirección completa (Portal del vocabulario callejero)

- **98 Construcciones catastrales**: Desde sótanos (-2, -1) hasta planta baja (00)
  - Diferentes usos: Enseñanza, Almacenamiento/Aparcamiento, Deportivo, Industrial, Comercial
  - Años de construcción: 2012
  - Identificadores: Escalera + Planta + Puerta (ej: 3/-2/01)
  - Áreas medidas en m²
  - Porcentajes de soporte (ej: 50.00%)

This complete example shows a cadastral parcel with all its information:

- **Cadastral Parcel**: `Parcela_8942103VK2793`
  - Cadastral reference: `8942103VK2793`
  - Classification: Urban
  - WKT geometry and area (407.586 m²)
  - Address: Calle Badajoz 348[B], 28223 Pozuelo de Alarcón, Madrid

- **Cadastral Property**: `Inmueble_8942103VK2793S0001UO`
  - Cadastral reference: `8942103VK2793S0001UO`
  - Participation: 100.00%
  - Use: Cultural
  - Classification: Urban
  - Complete address (Portal from callejero vocabulary)

- **98 Cadastral Constructions**: From basements (-2, -1) to ground floor (00)
  - Different uses: Educational, Storage/Parking, Sports, Industrial, Commercial
  - Construction years: 2012
  - Identifiers: Staircase + Floor + Door (ex: 3/-2/01)
  - Areas measured in m²
  - Support percentages (ex: 50.00%)

**Fuente**: Datos extraídos del documento oficial del Catastro: `8942103VK2793S0001UO.pdf`

**Source**: Data extracted from the official Cadastre document: `8942103VK2793S0001UO.pdf`

## 2. `8942103VK2793S0001UO.pdf`

Documento de referencia oficial del Catastro Español que contiene la información de origen de la parcela y sus inmuebles/construcciones.

Official reference document from the Spanish Cadastre containing the source information of the parcel and its properties/constructions.

# Validación de Ejemplos (Example Validation)

Para validar los ejemplos de esta carpeta, ejecute:

To validate the examples in this folder, run:

```bash
python tests/validate.py examples/*.ttl
```

Este comando ejecutará las siguientes validaciones:

This command will perform the following validations:

1. **Validación sintáctica RDF** - Verifica que los archivos Turtle sean sintácticamente correctos
2. **Consistencia de tipos** - Comprueba que las instancias pertenecen a las clases correctas
3. **Uso correcto de propiedades** - Valida que se utilizan las propiedades apropiadas según sus dominios y rangos
4. **Referencias a vocabularios externos** - Verifica que las referencias a GeoSPARQL, Callejero, y KOS son correctas

1. **RDF syntactic validation** - Verifies that Turtle files are syntactically correct
2. **Type consistency** - Checks that instances belong to the correct classes
3. **Correct property usage** - Validates that properties are used appropriately according to their domains and ranges
4. **References to external vocabularies** - Verifies that references to GeoSPARQL, Callejero, and KOS are correct

# Estructura de los Ejemplos (Example Structure)

Los ejemplos siguen esta estructura general:

The examples follow this general structure:

```turtle
@prefix : <https://edint.github.io/edint-ontologia-catastro/examples#> .
@prefix edintcat: <https://edint.github.io/edint-ontologia-inmuebles/ontology/catastro#> .
@prefix geo: <http://www.opengis.net/ont/geosparql#> .
@prefix skos: <http://www.w3.org/2004/02/skos/core#> .
@prefix callejero: <http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/callejero#> .
@prefix qudt: <http://qudt.org/schema/qudt/> .
@prefix qudtunit: <http://qudt.org/vocab/unit/> .
@prefix edintkos-use: <http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/> .
@prefix edintkos-clase: <http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/> .

# Example entity
:Example_Parcel
    a edintcat:CadastralParcel ;
    edintcat:hasCadastralReference :Ref_Example ;
    edintcat:hasClass edintkos-clase:Urban ;
    geo:hasGeometry :Example_Geometry .
```

# Referencias a Vocabularios (References to Vocabularies)

Los ejemplos integran los siguientes vocabularios externos:

The examples integrate the following external vocabularies:

- **GeoSPARQL** (`http://www.opengis.net/ont/geosparql#`) - Para geometrías y medidas espaciales
- **Callejero** (`http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/callejero#`) - Para direcciones españolas
- **KOS de Usos** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/`) - Para clasificación de usos catastrales
- **KOS de Clases** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/`) - Para clasificación urbana/rural
- **QUDT** (`http://qudt.org/schema/qudt/`) - Para unidades de medida (m², %)

- **GeoSPARQL** (`http://www.opengis.net/ont/geosparql#`) - For geometries and spatial measurements
- **Callejero** (`http://vocab.linkeddata.es/datosabiertos/def/urbanismo-infraestructuras/callejero#`) - For Spanish addresses
- **Use KOS** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/`) - For cadastral use classification
- **Class KOS** (`http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/`) - For urban/rural classification
- **QUDT** (`http://qudt.org/schema/qudt/`) - For measurement units (m², %)

# Notas Importantes (Important Notes)

1. **Prefijos**: Los ejemplos utilizan prefijos consistentes con la ontología y los vocabularios externos.
2. **URI de ejemplos**: Las instancias de ejemplo usan el prefijo `examples#` para distinguirlas de datos de producción.
3. **Integridad referencial**: Los ejemplos mantienen la integridad referencial completa (todas las referencias apuntan a entidades existentes).
4. **Validación**: Antes de usar los ejemplos, se recomienda validarlos con el script de validación.

1. **Prefixes**: Examples use consistent prefixes with the ontology and external vocabularies.
2. **Example URIs**: Example instances use the `examples#` prefix to distinguish them from production data.
3. **Referential integrity**: Examples maintain complete referential integrity (all references point to existing entities).
4. **Validation**: Before using examples, it is recommended to validate them with the validation script.

# Uso de los Ejemplos (Using the Examples)

Estos ejemplos pueden ser utilizados como:

These examples can be used as:

1. **Plantillas** (Templates) - Para crear nuevas instancias de entidades catastrales
2. **Casos de prueba** (Test cases) - Para validar consultas SPARQL en el directorio `requirements/`
3. **Documentación** (Documentation) - Para entender las relaciones entre entidades catastrales
4. **Integración de datos** (Data integration) - Como guía para convertir datos catastrales a Linked Data

1. **Templates** - To create new cadastral entity instances
2. **Test cases** - To validate SPARQL queries in the `requirements/` directory
3. **Documentation** - To understand relationships between cadastral entities
4. **Data integration** - As a guide for converting cadastral data to Linked Data
