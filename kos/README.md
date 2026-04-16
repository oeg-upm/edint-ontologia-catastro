# Implementación de vocabularios (Vocabularies Implementation)

Esta carpeta contiene los archivos de **implementación del vocabulario controlado o KOS (Sistemas de Organización del Conocimiento/ Knowledge Organization Systems)**, que representan la definición formal y legible por máquina de los vocabularios necesarios para la ontología del Catastro Español.

This folder contains the **implementation of controlled vocabulary or KOS (Knowledge Organization Systems)**, which represent the formal and machine-readable definition of the vocabularies necessary for the Spanish Cadastre Ontology.

# Vocabularios incluidos (Included Vocabularies)

Esta carpeta incluye tres vocabularios KOS principales del Catastro:

This folder includes three main KOS vocabularies of the Cadastre:

## 1. Vocabulario de Usos (`catastro-use.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/uso`
- **Versión**: 0.1.1
- **Conceptos**: 16 conceptos principales + jerarquía
- **Descripción**: Vocabulario de usos para el Catastro Español según RD 1020/1993

### Jerarquía de Usos (Uses Hierarchy)

El esquema de conceptos tiene los siguientes conceptos de nivel superior (Top Concepts):

The concept scheme has the following top-level concepts:

1. **Residencial** (Residential)
   - Uso: Vivienda (Housing)
   - Fuente: RD 1020/1993, Cuadro 1

2. **Industrial** (Industrial)
   - Uso: Actividades industriales y de producción
   - Fuente: RD 1020/1993, Cuadro 1

3. **Oficinas** (Offices)
   - Uso: Actividades administrativas, corporativas y despachos
   - Fuente: RD 1020/1993, Cuadro 1

4. **Comercial** (Commercial)
   - Uso: Comercio y venta al por menor
   - Fuente: RD 1020/1993, Cuadro 1

5. **Deportes** (Sports)
   - Uso: Actividades deportivas
   - Fuente: RD 1020/1993, Cuadro 1

6. **Espectáculos** (Entertainment)
   - Uso: Espectáculos públicos, cines y teatros
   - Fuente: RD 1020/1993, Cuadro 1

7. **Ocio y Hostelería** (Leisure and Hospitality)
   - Uso: Alojamiento turístico, restaurantes y servicios de ocio
   - Fuente: RD 1020/1993, Cuadro 1
   - Etiqueta alternativa: Turístico (Tourist)

8. **Sanidad y Beneficencia** (Healthcare and Charity)
   - Uso: Hospitales, clínicas y beneficencia
   - Fuente: RD 1020/1993, Cuadro 1

9. **Cultural** (Cultural)
   - Uso: Museos, bibliotecas y exposiciones culturales
   - Fuente: RD 1020/1993, Cuadro 1

10. **Religioso** (Religious)
   - Uso: Actividades religiosas
   - Fuente: RD 1020/1993, Cuadro 1

11. **Educativo** (Educational)
   - Uso: Actividades educativas (escuelas, universidades)
   - Fuente: RD 1020/1993, Cuadro 1

12. **Singular** (Singular)
   - Uso: Inmuebles singulares de carácter especial
   - Fuente: RD 1020/1993, Cuadro 1

13. **Almacenamiento/Aparcamiento** (Storage and Parking)
   - Uso: Almacenes, garajes y aparcamientos
   - Fuente: RD 1020/1993, Cuadro 1

14. **Agricultural** (Agricultural)
   - Uso: Actividades agrícolas y ganaderas
   - Fuente: RD 1020/1993, Cuadro 1

15. **Espacios Verdes** (Green Spaces)
   - Uso: Parques, jardines y zonas verdes
   - Fuente: RD 1020/1993, Cuadro 1

16. **Otro** (Other)
   - Uso: Usos no especificados en las categorías anteriores
   - Fuente: RD 1020/1993, Cuadro 1

1. **Residencial** (Residential)
   - Use: Vivienda (Housing)
   - Source: RD 1020/1993, Table 1

2. **Industrial** (Industrial)
   - Use: Industrial activities and production
   - Source: RD 1020/1993, Table 1

3. **Oficinas** (Offices)
   - Use: Administrative, corporate and professional office activities
   - Source: RD 1020/1993, Table 1

4. **Comercial** (Commercial)
   - Use: Commerce and retail business activities
   - Source: RD 1020/1993, Table 1

5. **Deportes** (Sports)
   - Use: Sports activities
   - Source: RD 1020/1993, Table 1

6. **Espectáculos** (Entertainment)
   - Use: Public shows, cinemas and theaters
   - Source: RD 1020/1993, Table 1

7. **Ocio y Hostelería** (Leisure and Hospitality)
   - Use: Tourist accommodation, restaurants and leisure services
   - Source: RD 1020/1993, Table 1
   - Alternative label: Turístico (Tourist)

8. **Sanidad y Beneficencia** (Healthcare and Charity)
   - Use: Hospitals, clinics and charitable institutions
   - Source: RD 1020/1993, Table 1

9. **Cultural** (Cultural)
   - Use: Museums, libraries and cultural exhibitions
   - Source: RD 1020/1993, Table 1

10. **Religioso** (Religious)
   - Use: Religious activities
   - Source: RD 1020/1993, Table 1

11. **Educativo** (Educational)
   - Use: Educational activities (schools, universities)
   - Source: RD 1020/1993, Table 1

12. **Singular** (Singular)
   - Use: Singular properties of special character
   - Source: RD 1020/1993, Table 1

13. **Almacenamiento/Aparcamiento** (Storage and Parking)
   - Use: Warehouses, garages and parking lots
   - Source: RD 1020/1993, Table 1

14. **Agricultural** (Agricultural)
   - Use: Agricultural and livestock activities
   - Source: RD 1020/1993, Table 1

15. **Espacios Verdes** (Green Spaces)
   - Use: Parks, gardens and green zones
   - Source: RD 1020/1993, Table 1

16. **Otro** (Other)
   - Use: Uses not specified in previous categories
   - Source: RD 1020/1993, Table 1

### Ejemplo de uso (Usage Example)

```turtle
@prefix edintkos-use: <http://vocab.linkeddata.es/datosabiertos/kos/edint/uso/> .

:MyProperty edintcat:hasUse edintkos-use:Educational .
```

---

## 2. Vocabulario de Clasificaciones (`catastro-clase.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/clase`
- **Versión**: 0.1.2
- **Conceptos**: 8 conceptos principales + jerarquía
- **Descripción**: Vocabulario de clasificación de inmuebles según RDLeg 1/2004

### Jerarquía de Clases (Classes Hierarchy)

El esquema de conceptos tiene 3 conceptos de nivel superior:

The concept scheme has 3 top-level concepts:

#### A. Urbano (Urban)

- **Descripción**: Inmueble clasificado como urbano en función de la naturaleza de su suelo, de acuerdo con la legislación urbanística aplicable.
- **Fuente legal**: RDLeg 1/2004, Artículo 7
- **Definición**: Property classified as urban based on the nature of its soil, in accordance with applicable urban planning legislation.
- **Definición**: Inmueble clasificado como urbano en función de la naturaleza de su suelo, de acuerdo con la legislación urbanística aplicable.

#### B. Rústico (Rural)

- **Descripción**: Inmueble clasificado como rústico en función de la naturaleza de su suelo, excluyendo expresamente aquellos designados como urbanos o de características especiales.
- **Fuente legal**: RDLeg 1/2004, Artículo 7
- **Definición**: Property classified as rural based on the nature of its soil, explicitly excluding those designated as urban or special.
- **Definición**: Inmueble clasificado como rústico en función de la naturaleza de su suelo, excluyendo expresamente aquellos designados como urbanos o de características especiales.

#### C. BICES - Bienes Inmobiliarios de Características Especiales

El concepto BICES agrupa 4 subcategorías de bienes de características especiales:

The BICES concept groups 4 subcategories of special characteristic properties:

##### C1. Infraestructuras de Energía y Refino (Energy and Refining Infrastructure) - BICES-A

- **Descripción**: Inmuebles destinados a la producción de energía eléctrica y gas y al refino de petróleo, y las centrales nucleares.
- **Fuente legal**: RDLeg 1/2004, Artículo 8.2, Grupo A
- **Definición**: Properties destined for the production of electrical energy and gas, oil refining, and nuclear power plants.
- **Definición**: Inmuebles destinados a la producción de energía eléctrica y gas y al refino de petróleo, y las centrales nucleares.

##### C2. Presas y Embalses (Dams and Reservoirs) - BICES-B

- **Descripción**: Las presas, saltos de agua y embalses, incluido su lecho o vaso, excepto las destinadas exclusivamente al riego.
- **Fuente legal**: RDLeg 1/2004, Artículo 8.2, Grupo B
- **Definición**: Dams, waterfalls and reservoirs, including their bed or basin, except those destined exclusively for irrigation.
- **Definición**: Las presas, saltos de agua y embalses, incluido su lecho o vaso, excepto las destinadas exclusivamente al riego.

##### C3. Autopistas de Peaje y Túneles (Toll Roads and Tunnels) - BICES-C

- **Descripción**: Las autopistas, carreteras y túneles de peaje.
- **Fuente legal**: RDLeg 1/2004, Artículo 8.2, Grupo C
- **Definición**: Toll highways, toll roads, and toll tunnels.
- **Definición**: Las autopistas, carreteras y túneles de peaje.

##### C4. Aeropuertos y Puertos Comerciales (Airports and Commercial Ports) - BICES-D

- **Descripción**: Los aeropuertos y puertos comerciales.
- **Fuente legal**: RDLeg 1/2004, Artículo 8.2, Grupo D
- **Definición**: Airports and commercial ports.
- **Definición**: Los aeropuertos y puertos comerciales.

### Ejemplo de clasificación (Classification Example)

```turtle
@prefix edintkos-clase: <http://vocab.linkeddata.es/datosabiertos/kos/edint/clase/> .

:MyParcel edintcat:hasClass edintkos-clase:Urban .
:MyRuralProperty edintcat:hasClass edintkos-clase:Rural .
:MyDam edintcat:hasClass edintkos-clase:BICES-B .
```

---

## 3. Vocabulario de Estados de Conservación (`catastro-estado.ttl`)

- **URI**: `http://vocab.linkeddata.es/datosabiertos/kos/edint/estado`
- **Versión**: 0.1.1
- **Conceptos**: 5 conceptos
- **Descripción**: Vocabulario de estados de conservación de construcciones según RD 1020/1993

### Estados de Conservación (Conservation States)

Los estados de conservación se definen en la Norma 14 de las Normas Técnicas de Valoración (RD 1020/1993):

Conservation states are defined in Standard 14 of the Technical Valuation Norms (RD 1020/1993):

1. **Nuevo** (New) - Construcción de reciente creación
2. **Bueno** (Good) - Estado de conservación satisfactorio
3. **Normal** (Normal) - Estado de conservación aceptable
4. **Deficiente** (Deficient) - Estado de conservación insuficiente
5. **Ruinoso** (Ruinous) - Estado de conservación muy deteriorado

1. **Nuevo** (New) - Recently built construction
2. **Bueno** (Good) - Satisfactory conservation state
3. **Normal** (Normal) - Acceptable conservation state
4. **Deficiente** (Deficient) - Insufficient conservation state
5. **Ruinoso** (Ruinous) - Very deteriorated conservation state

**Nota**: Este vocabulario está disponible en la ontología pero no está integrado actualmente en la ontología del Catastro como una propiedad de datatype. Se puede usar en futuras extensiones.

**Note**: This vocabulary is available in the ontology but is not currently integrated in the Cadastre ontology as a datatype property. It can be used in future extensions.

### Ejemplo de estado de conservación (Conservation State Example)

```turtle
@prefix edintkos-estado: <http://vocab.linkeddata.es/datosabiertos/kos/edint/estado/> .

:MyConstruction a :Property ;
    edintcat:hasConservationState edintkos-estado:Normal .
```

---

# Uso de los Vocabularios en la Ontología (Usage of Vocabularies in Ontology)

Los vocabularios KOS se integran en la ontología del Catastro a través de las siguientes propiedades:

The KOS vocabularies are integrated in the Cadastre ontology through the following properties:

### Para Usos (For Uses)

```turtle
?property a edintcat:CadastralProperty ;
          edintcat:hasUse ?use .

?use a skos:Concept ;
     skos:inScheme <http://vocab.linkeddata.es/datosabiertos/kos/edint/uso> .
```

### Para Clases (For Classes)

```turtle
?parcel a edintcat:CadastralParcel ;
        edintcat:hasClass ?class .

?class a skos:Concept ;
      skos:inScheme <http://vocab.linkeddata.es/datosabiertos/kos/edint/clase> .
```

### Para Estados (For States)

```turtle
?construction a edintcat:CadastralConstruction ;
               edintcat:hasConservationState ?state .

?state a skos:Concept ;
       skos:inScheme <http://vocab.linkeddata.es/datosabiertos/kos/edint/estado> .
```

---

# Fuentes Legales (Legal Sources)

Todos los vocabularios están alineados con las leyes españolas correspondientes:

All vocabularies are aligned with the corresponding Spanish laws:

- **Usos**: [Real Decreto 1020/1993](https://www.boe.es/buscar/act.php?id=BOE-A-1993-19265), Norma de Valoración, Anexo - Cuadro 1
- **Clases**: [Real Decreto Legislativo 1/2004](https://www.boe.es/buscar/act.php?id=BOE-A-2004-4163), Ley del Catastro Inmobiliario, Artículos 7 y 8
- **Estados**: [Real Decreto 1020/1993](https://www.boe.es/buscar/act.php?id=BOE-A-1993-19265), Norma 14 (Estado de Conservación)

- **Uses**: [Royal Decree 1020/1993](https://www.boe.es/buscar/act.php?id=BOE-A-1993-19265), Valuation Standard, Annex - Table 1
- **Classes**: [Royal Legislative Decree 1/2004](https://www.boe.es/buscar/act.php?id=BOE-A-2004-4163), Real Estate Cadastre Law, Articles 7 and 8
- **States**: [Royal Decree 1020/1993](https://www.boe.es/buscar/act.php?id=BOE-A-1993-19265), Standard 14 (Conservation State)

---

# Propósito (Purpose)

El objetivo de esta carpeta es almacenar los archivos de los **vocabularios controlados o KOS**, que describen los conceptos y las relaciones entre ellos, utilizados por la ontología del Catastro Español.

The goal of this folder is to store the files of the **controlled vocabularies or KOS**, which describe the concepts and the relationships between them, used by the Spanish Cadastre Ontology.

---

# Formatos aceptados (Accepted Formats)

Incluya recursos en los siguientes formatos:

Include resources in the following formats:

- `.owl` — Ficheros Ontology Web Language files  
- `.rdf` — Ficheros  Resource Description Framework files  
- `.ttl` — Serialización en Turtle (recomendado)   
- `.jsonld` — JSON para datos enlazados

- `.owl` — Ontology Web Language files
- `.rdf` — Resource Description Framework files
- `.ttl` — Turtle serialization (recommended)
- `.jsonld` — JSON for linked data

---

# Buenas prácticas (Best Practices)

- Mantenga las versiones del vocabulario o KOS claramente etiquetados y documentados.
- Valide la sintaxis y semántica antes de realizar cambios.
- Mantenga la coherencia con los diagramas conceptuales y la documentación almacenados en la carpeta de conceptualización, si corresponde.
- Utilice una estrategia estandarizada de espacios de nombres y prefijos.
- Asegure que todos los conceptos tengan prefLabels en español e inglés.

- Keep vocabulary or KOS versions clearly labeled and documented.
- Validate syntax and semantics before making changes.
- Maintain consistency with conceptual diagrams and documentation stored in the conceptualization folder, if applicable.
- Use a standardized namespace and prefix strategy.
- Ensure all concepts have prefLabels in Spanish and English.

---

# Notas (Notes)

- Esta carpeta debe contener únicamente **archivos de implementación** — no diagramas, notas ni documentación.
- Considere mantener un registro de cambios o un archivo de historial de versiones si se mantienen múltiples versiones de los vocabularios.

- This folder should contain only **implementation files** — no diagrams, notes or documentation.
- Consider maintaining a change log or version history file if multiple versions of vocabularies are maintained.
