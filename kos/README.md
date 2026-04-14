# Implementación de vocabularios

Esta carpeta contiene los archivos de **implementación del vocabulario controlado o KOS (Sistemas de Organización del Conocimiento/ Knowledge Organization Systems)**, que representan la definición formal y legible por máquina de los vocabularios necesarios.

# Vocabularios incluidos

## 1. Uso Catastro (`catastro-use.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/uso`
- **Descripción**: Vocabulario de usos para el catastro español.
- **Clases principales**: Conceptos SKOS para diferentes tipos de uso (residencial, comercial, industrial, etc.)

## 2. Estado Catastro (`catastro-estado.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/estado`
- **Descripción**: Vocabulario de estados para el catastro español.
- **Clases principales**: Conceptos SKOS para diferentes estados (activo, inactivo, etc.)

## 3. Clase Catastro (`catastro-clase.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/clase`
- **Descripción**: Vocabulario de clases para el catastro español.
- **Clases principales**: Conceptos SKOS para diferentes clases de inmuebles.

# Propósito

El objetivo de esta carpeta es almacenar los archivos de los **vocabularios controlados o KOS**, que describen los conceptos y las relaciones entre ellos.


# Formatos aceptados

Incluya recursos en los siguientes formatos:

- `.owl` — Ficheros Ontology Web Language files  
- `.rdf` — Ficheros  Resource Description Framework files  
- `.ttl` — Serialización en Turtle   
- `.jsonld` — JSON para datos enlazados

# Buenas prácticas

- Mantenga las versiones del vocabulario o KOS claramente etiquetadas y documentadas.
- Valide la sintaxis y semántica antes de realizar cambios.
- Mantenga la coherencia con los diagramas conceptuales y la documentación almacenados en la carpeta de conceptualización, si corresponde.
- Utilice una estrategia estandarizada de espacios de nombres y prefijos.


# Notas

- Esta carpeta debe contener únicamente **archivos de implementación** — no diagramas, notas ni documentación.
- Considere mantener un registro de cambios o un archivo de historial de versiones si se mantienen múltiples versiones de los vocabularios.
