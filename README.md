# Ejemplos de schema orientados a E-E-A-T

Este repositorio recoge **ejemplos reales de schema** pensados para reforzar la **experiencia, el conocimiento, la autoridad y la credibilidad (E-E-A-T)** en proyectos digitales.

No están diseñados para activar *rich results* ni para forzar elementos visuales en buscadores.
Su objetivo es mejorar la **claridad de entidades**, la **autoría responsable** y la **coherencia editorial**, especialmente en contextos donde la credibilidad del autor no debe depender de un único dominio o proyecto.

Idioma principal: español (España).

---

## Por qué existe este repositorio

En muchos proyectos SEO, el marcado de datos se trata como una tarea técnica aislada, orientada a cumplir validadores o a obtener snippets.

En la práctica, el schema resulta más valioso cuando ayuda a que buscadores y sistemas basados en IA entiendan correctamente:

- Quién es responsable del contenido
- Qué experiencia real tiene un autor
- Qué relación existe entre autor, organización y proyecto
- Dónde están los límites de la responsabilidad editorial

Estos ejemplos nacen de ese enfoque y de su aplicación en proyectos reales.

---

## Qué NO es este repositorio

- No es una colección de plantillas para copiar y pegar  
- No es una guía exhaustiva de Schema.org  
- No está pensada para plugins ni CMS concretos  
- No persigue mejoras directas de ranking  

Cada archivo asume **criterio, contexto y adaptación**.

---

## Propiedades clave utilizadas y por qué importan

Los ejemplos de este repositorio **no intentan cubrir todo Schema.org**.
Se centran únicamente en propiedades que aportan señales reales de E-E-A-T.

### Experiencia (Experience)

Propiedades utilizadas para reflejar **trayectoria y trabajo real**, no solo conocimiento teórico:

- `subjectOf`
- `isBasedOn`
- `temporalCoverage`
- `mainEntityOfPage`

Estas propiedades ayudan a contextualizar **qué se ha hecho**, durante cuánto tiempo y en qué tipo de escenarios.
---

### Conocimiento (Expertise)

Propiedades orientadas a definir **ámbitos de conocimiento claros y acotados**:

- `knowsAbout`
- `hasOccupation`
- `alumniOf`
- `hasCredential`
- `additionalType`

El objetivo no es enumerar habilidades, sino **delimitar especialización real**.

---

### Autoridad (Authority)

Propiedades que permiten establecer **relaciones entre entidades** y referencias externas:

- `sameAs`
- `worksFor`
- `founder`
- `memberOf`
- `publisher`
- `isPartOf`

La autoridad no se construye con claims internos, sino con relaciones coherentes.

---

### Credibilidad y confianza (Trust)

Propiedades que explicitan **criterios editoriales, límites y responsabilidad**:

- `publishingPrinciples`
- `ethicsPolicy`
- `correctionPolicy`
- `citation`
- `contactPoint`
- `legalName`
- `ownershipFundingInfo`

Estas señales son especialmente relevantes en verticales sensibles o volátiles.

---

## Uso de Wikipedia y Wikidata como apoyo a E-E-A-T

En este repositorio, Wikipedia y Wikidata se utilizan como **fuentes de referencia externas** para reducir ambigüedad y mejorar la comprensión de entidades por parte de buscadores y sistemas basados en IA.
No se usan como señales de ranking, sino como **mecanismo de desambiguación y contexto**.

---

### Identidades propias vs. temáticas

Es importante diferenciar dos usos distintos:

#### Wikipedia / Wikidata de la entidad (identidad)

Cuando una persona u organización **tiene entrada propia** en Wikipedia o Wikidata, puede utilizarse en propiedades como:

- `sameAs` (Profile Person u Organization)

En este caso, Wikipedia/Wikidata actúan como **identidades externas verificables**.

Si no existe una entrada propia, **no debe forzarse**. Es preferible limitar `sameAs` a perfiles oficiales reales.

---

#### Wikipedia / Wikidata del tema (contenido)

Cuando una página o contenido trata sobre un **concepto, disciplina o tema concreto**,
puede utilizarse Wikipedia/Wikidata para contextualizar ese tema mediante:

- `about`
- `knowsAbout` (en perfiles de autor u organización)

En este caso, Wikipedia/Wikidata **no representan a la entidad**, sino al **concepto tratado**.

---

### Criterios para elegir el artículo correcto

Antes de enlazar un artículo de Wikipedia o Wikidata, conviene comprobar que:

- No es una página de desambiguación
- No es una categoría o portal
- La definición inicial encaja con el contenido real de la página
- La granularidad es adecuada (mejor el concepto específico que el genérico)

Si no existe un artículo suficientemente preciso, es preferible:
- usar solo `name` sin `sameAs`
- o esperar a disponer de una referencia adecuada

---

### Buenas prácticas

- No mezclar Wikipedia/Wikidata de la entidad con la del tema
- No enlazar conceptos irrelevantes solo por “completar” el schema
- No utilizar más de 1–3 referencias temáticas por página
- Priorizar coherencia entre lo que ve el usuario y lo que se marca en schema

El objetivo es siempre el mismo:
**dejar claro quién es la entidad y de qué trata el contenido**, sin atajos.

---

## Diferencia entre Profile Person y Author schema

En este repositorio se diferencia de forma explícita entre dos niveles que suelen mezclarse incorrectamente:

### Profile Person (entidad de identidad)

Representa a la **persona como entidad estable**.
No depende de un contenido concreto ni de un proyecto específico.

Se utiliza para:
- Definir identidad y trayectoria
- Delimitar ámbitos de conocimiento
- Conectar perfiles externos verificables
- Sostener señales de E-E-A-T a largo plazo

Este nivel **no debería reescribirse** en función de cada artículo.

---

### Author schema (rol editorial)

Representa a la **persona en su rol de autor dentro de un contenido concreto**.

Se utiliza para:
- Atribuir responsabilidad editorial
- Contextualizar experiencia aplicada
- Explicar desde qué posición se escribe
- Reflejar relación con una organización o proyecto

Este nivel **sí es contextual** y puede variar según:
- el tipo de contenido
- el proyecto
- el momento temporal

El author **no es la página de perfil**.
Es la persona actuando como autora en un contexto específico.

Separar correctamente estos dos niveles es clave para que la credibilidad del autor no se pierda cuando los proyectos cambian o desaparecen.

---

## Convención de uso de propiedades

Para evitar interpretaciones incorrectas o copias mecánicas, este repositorio utiliza
la siguiente convención:

- *Propiedades en cursiva*  
  Deben **revisarse, adaptarse o completarse** según el contexto real del proyecto, especialmente en el Author schema.

- Propiedades en texto normal  
  Forman parte de la **estructura del modelo de entidad** y no deberían modificarse sin un motivo claro, ya que alteran la coherencia del grafo.

Esta distinción es intencionada y responde a experiencia real en proyectos donde pequeños cambios rompen la interpretación de entidades.

Ejemplo:

- `knowsAbout`
- *`sameAs`*
- `hasOccupation`
- *`temporalCoverage`*

---

## Archivos incluidos

### `person-eeat.json`

Ejemplo de schema para una **entidad de autor real (Profile Person)**.

Enfoque:
- Identidad estable
- Especialización delimitada
- Contexto temporal
- Enlaces a perfiles externos verificables

---

### `organization-eeat.json`

Ejemplo de schema para una organización entendida como **editor o publicador**, no como sustituto de la autoridad del autor.

---

### `author-external.json`

Modelo de **autor externo al proyecto** (Author schema).

Pensado para escenarios en los que:
- El autor no pertenece al dominio
- Los proyectos pueden cambiar o desaparecer
- La credibilidad del autor debe mantenerse independiente

---

### `publishing-principles.json`

Representación estructurada de **principios editoriales y éticos**.

Define:
- Cómo se toman decisiones de contenido
- Qué se revisa y qué no
- Dónde termina la responsabilidad del autor

Este archivo existe para reforzar **confianza**, no para SEO técnico.

---

## Nota final

El marcado de datos no genera confianza por sí mismo.

La confianza se construye cuando:
- Las entidades son coherentes
- La experiencia está documentada
- Los límites son explícitos
- La responsabilidad es clara

Estos ejemplos intentan reflejar ese principio.

Autor: Verónica Llana Celada (ORCID: https://orcid.org/0000-0003-0876-2344)
DOI: https://doi.org/10.5281/zenodo.18148283
