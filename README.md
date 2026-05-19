# Ontología para la representación del Catastro Inmobiliario Español

Esta ontología permite representar el dominio del Catastro Inmobiliario Español, centrada en parcelas catastrales, inmuebles catastrales y construcciones catastrales.

Está siendo desarrollada en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es/)).

# Propósito y alcance de la ontología

El propósito de esta ontología es modelar las entidades y relaciones fundamentales del Catastro Inmobiliario Español para habilitar la interoperabilidad de datos catastrales en el contexto de los datos enlazados (Linked Data). El alcance se limita a parcelas catastrales, inmuebles catastrales, construcciones catastrales, referencias catastrales, direcciones, usos y clasificaciones, y geometrías y áreas. Quedan fuera del alcance aspectos como titularidad de bienes, valoración catastral, datos de transmisiones y procesos administrativos.

# Prefijo y espacio de nombres

El prefijo de esta ontología es `edintcat`. Se publica en el espacio de nombres: http://vocab.linkeddata.es/datosabiertos/def/catastro/

# Modelo conceptual (Ontology conceptualization)

![Diagrama del modelo conceptual](diagrams/diagram.png)

# Estructura del repositorio (Repository structure)

| Carpeta | Descripción |
|--------|--------------|
| **diagrams/**     | Almacena diagramas y otros recursos que representan el modelo conceptual de la ontología (por ejemplo, jerarquías de clases, relaciones).                                     |
| **documentation/**         | Almacena la documentación HTML u orientada a humanos de la ontología y artefactos relacionados.                                                                               |
| **examples/**     | Incluye ejemplos que demuestran cómo instanciar o aplicar la ontología en escenarios de datos reales.                                                                         |
| **kos/**          | Almacena vocabularios controlados o implementación de KOS, generalmente implementaciones SKOS en RDF.                                                                         |
| **ontology/**     | Contiene los archivos de implementación reales de la ontología en formatos como `.owl`, `.rdf`, `.ttl` o `.jsonld`.                                                           |
| **requirements/** | Contiene todos los documentos utilizados para definir los requisitos de la ontología: ejemplos de datos, preguntas de competencia, requisitos funcionales, casos de uso, etc. |
| **shapes/**       | Contiene los SHACL shapes utilizadas para definir y validar las restricciones de la ontología.                                                                                |


# Mantenimiento y evolución (Maintenance and evolution)

Para manejar las incidencias o mejoras sugeridas con respecto a la ontología, recomendamos seguir las guías proporcionadas en ([Issues Management](./ISSUES.md)) para generar una incidencia.

# Financiación (Funding)

Esta ontología ha sido desarrollada en el contexto del Espacio de Datos para las Infraestructuras Urbanas Inteligentes ([EDINT](https://edint.es)).

![Logos](./resources/EDINT_UE_V-Color.png)
