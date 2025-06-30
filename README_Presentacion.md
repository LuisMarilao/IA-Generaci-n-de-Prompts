# Lector de percepción pública político-social
![alt text](image.png)

### Nombre del proyecto
**Lector de percepción pública político-social**

### Presentación del problema a abordar
En el contexto sociopolítico chileno de 2025, el país enfrenta tensiones recurrentes relacionadas con demandas sociales, conflictos institucionales y desconfianza en la clase política. Los medios de comunicación y las declaraciones públicas de figuras políticas y sociales son una fuente constante de información para la ciudadanía, pero también de confusión y polarización.

Actualmente, no existen herramientas accesibles para que personas no especializadas puedan analizar de forma estructurada el contenido y el impacto de estas noticias. Esto dificulta la comprensión crítica del entorno, limita la participación ciudadana y obstaculiza la formulación de respuestas informadas por parte de distintos actores sociales, como organizaciones civiles, investigadores o instituciones educativas.

Este proyecto busca responder a esa necesidad mediante el desarrollo de un sistema de análisis automatizado, basado en técnicas de prompt engineering aplicadas a modelos de lenguaje (como GPT), que permita extraer de manera sistemática:

El contexto y lenguaje dominante de cada noticia.

Las tensiones sociales o políticas presentes.

Los actores involucrados y su rol.

Los impactos y respuestas institucionales.

La afectación a grupos vulnerables.

Posibles reacciones de la opinión pública.

Además, una segunda capa de análisis permitirá relacionar los distintos casos entre sí y proponer iniciativas para abordar las problemáticas identificadas, fomentando una visión estratégica, democrática y propositiva.

Esta solución, diseñada desde una perspectiva interdisciplinaria y rigurosa, tiene el potencial de apoyar a diversos sectores: ciudadanía, periodistas, educadores, investigadores, tomadores de decisiones y estudiantes.


## Desarrollo de la propuesta de solución

La propuesta consiste en desarrollar un modelo de prompting que reciba resumenes de noticias chilenas y extraiga información según los siguiente puntos
1. Contexto  
2. Lenguaje dominante (técnico, emocional, populista, institucional, etc.)  
3. Tensión social o política (si la hay, especificar)  
4. Actores involucrados  
5. Nivel de impacto (local, regional, nacional, internacional)  
6. Tipo de acción del Estado (política pública, sanción, transparencia, etc.)  
7. Valor democrático comprometido (transparencia, legalidad, representación, etc.)
8. Grupo social afectado o vulnerable (si aplica)
9. Reacción probable de la opinión pública  
10. Institución o tipo de fuente mencionada

. El análisis se realiza mediante técnicas de NLP orientadas por modelos de lenguaje  GPT 3.5, aplicados a un contexto chileno de 2025.

### Prompt base:

Prompt I:
Analiza las siguientes noticias públicas del acontecer chileno realizadas en el último tiempo del año 2025.

Para cada una de ellas, entrega el análisis en una tabla con las siguientes filas:

1. Contexto  
2. Lenguaje dominante (técnico, emocional, populista, institucional, etc.)  
3. Tensión social o política (si la hay, especificar)  
4. Actores involucrados  
5. Nivel de impacto (local, regional, nacional, internacional)  
6. Tipo de acción del Estado (política pública, sanción, transparencia, etc.)  
7. Valor democrático comprometido (transparencia, legalidad, representación, etc.)
8. Grupo social afectado o vulnerable (si aplica)
9. Reacción probable de la opinión pública  
10. Institución o tipo de fuente mencionada

Lista de noticias

Prompt II:
Analiza la siguiente tabla de análisis de noticias públicas del acontecer chileno, notando relaciones entre las distintas noticias y sus implicancias sociales,políticas y económicas.
Entrega propuestas de iniciativas o acciones que podrían tomarse para abordar las problemáticas identificadas.

Tabla de análisis

## Justificación de la viabilidad del proyecto

Técnicamente, el proyecto es viable dentro del marco del curso y el tiempo disponible. Utiliza técnicas de prompting avanzadas en un entorno controlado, sin requerir el entrenamiento de modelos desde cero. Las herramientas utilizadas (OpenAI API, Jupyter Notebook) son accesibles y compatibles con la infraestructura actual. Además, el enfoque por prompting reduce la necesidad de grandes datasets etiquetados.

## Objetivos

### Objetivo general:
Desarrollar un sistema de análisis socio-político automatizado basado en lenguaje natural para noticias chilenas recientes.

### Objetivos específicos:
- Diseñar prompts robustos que identifiquen tensiones en distintos puntos claves.
- Aplicar el sistema a noticias reales desde sitios web de confianza.
- Evaluar la utilidad del análisis para distintos usuarios: ciudadanos, investigadores, comunicadores.

## Metodología

1. **Diseño de prompt:** creación y refinamiento del prompt central.
2. **Recolección de datos:** uso de noticias reales en medios nacionales confiables. Es esta fase, se ingresas de forma manual.
3. **Procesamiento:** aplicación del prompt I a los textos mediante GPT.
4. **Análisis y visualización:** extracción de frases clave y categorización en una tabla.
5. **Procesamiento_2:** aplicación de prompt II a tabla de análisis resultante de prompt I
6. **Análisis e Iniciativas:** Resultados de análisis general y relacional de las noticias, junto con recomendaciones de iniciativas. 

## Herramientas y tecnologías

- **Lenguaje:** Python (en Jupyter Notebook).
- **Modelo:** OpenAI GPT 3.5 (usando la API).
- **Técnica de prompting:** Zero-shot y few-shot prompting.
- **Librerías:** `openai`, `pandas`, entre otras.

El uso de **zero-shot prompting** permite analizar textos sin necesidad de entrenamiento previo, adaptándose fácilmente a nuevos discursos.
 **Few-shot prompting** se usa en el primer prompt para parametrizar el resultado del primer análisis

## Implementación

El archivo Jupyter adjunto (`fast_prompting_en_accion.ipynb`) contiene:

- La estructura modular para ejecutar prompts.
- Código de conexión con la API de OpenAI.
- Pruebas iniciales con discursos y resultados clasificados.


## Nombre estudiante: Luis Ignacio Marilao Lepicheo