# Guía para Educadores y Docentes

¡Bienvenido, colega educador! Esta guía está diseñada para profesores universitarios, instructores de bootcamps, facilitadores de comunidades técnicas y líderes de grupos de estudio que deseen adoptar este plan de estudios en sus cursos de Ciencia de Datos.

El currículo **Ciencia de Datos para Principiantes** fue concebido bajo principios sólidos de pedagogía activa, diseño curricular inverso (*Backward Design*) y aprendizaje basado en proyectos (*Project-Based Learning*).

---

## Tabla de Contenidos

- [Filosofía y Metodología Pedagógica](#filosofía-y-metodología-pedagógica)
- [Estructura Didáctica de Cada Lección](#estructura-didáctica-de-cada-lección)
- [Propuestas de Cronograma y Adaptación](#propuestas-de-cronograma-y-adaptación)
  - [Opción A: Formato Intensivo de 10 Semanas (2 lecciones por semana)](#opción-a-formato-intensivo-de-10-semanas-2-lecciones-por-semana)
  - [Opción B: Semestre Académico de 16 Semanas](#opción-b-semestre-académico-de-16-semanas)
- [Uso con GitHub Classroom](#uso-con-github-classroom)
- [Evaluación y Rúbricas Formativas](#evaluación-y-rúbricas-formativas)
- [Manejo de Dudas y Dinámicas de Aula](#manejo-de-dudas-y-dinámicas-de-aula)
- [Consideraciones Éticas y Pensamiento Crítico](#consideraciones-éticas-y-pensamiento-crítico)

---

## Filosofía y Metodología Pedagógica

En la enseñanza de la Ciencia de Datos, uno de los errores más frecuentes es reducir la disciplina a la sintaxis de librerías o a la memorización mecánica de fórmulas matemáticas. Nuestra propuesta formativa articula tres pilares inseparables:

1. **Comprensión Conceptual Profunda**: El estudiante comprende *por qué* se utiliza una técnica antes de implementarla (ej. por qué estandarizar variables antes de aplicar PCA o K-Means, o cuál es el riesgo de multicolinealidad).
2. **Práctica Activa y Continua**: Las explicaciones teóricas se alternan inmediatamente con celdas de código en Jupyter Notebooks, permitiendo a los alumnos experimentar, cometer errores y observar los efectos de cada transformación de datos.
3. **Criterio Ético y de Negocio**: Cada análisis debe traducirse en un entendimiento riguroso del contexto y en ideas accionables, evaluando siempre el sesgo algorítmico (*bias*) y la privacidad de las personas.

---

## Estructura Didáctica de Cada Lección

Cada una de las 20 lecciones sigue una secuencia pedagógica estandarizada de 5 fases:

1. **Gancho y Motivación Visual (*Hook*)**: 
   - Se inicia con la **Sketchnote** de la lección para activar la memoria visual y presentar el mapa conceptual.
   - Video introductorio breve con el planteamiento del desafío del mundo real.
2. **Activación de Conocimientos Previos**:
   - **Cuestionario previo (*Pre-lecture quiz*)**: 3 preguntas diagnósticas diseñadas no para calificar con fines punitivos, sino para identificar lagunas y despertar curiosidad.
3. **Desarrollo Teórico y Conceptual**:
   - Lectura técnica con rigor matemático y contextualización en español latino, preservando los términos técnicos nativos de la industria (*DataFrames*, *Pipelines*, *Overfitting*, etc.).
4. **Laboratorio Interactivo (*Hands-on Coding*)**:
   - Cuaderno Jupyter (`notebook.ipynb`) guiado con código ejecutable paso a paso, ejercicios de completación y retos analíticos.
5. **Evaluación de Consolidación y Proyecto**:
   - **Cuestionario posterior (*Post-lecture quiz*)**: 3 preguntas de evaluación formativa.
   - **Tarea / Proyecto de aplicación (`assignment.md`)**: Trabajo autónomo que requiere aplicar la técnica a un conjunto de datos nuevo.

---

## Propuestas de Cronograma y Adaptación

### Opción A: Formato Intensivo de 10 Semanas (2 lecciones por semana)
Ideal para bootcamps, cursos de verano o diplomados técnicos (4 a 6 horas lectivas semanales + trabajo autónomo):

- **Semana 1**: Lecciones 01 (Definiendo la Ciencia de Datos) y 02 (Ética en Ciencia de Datos).
- **Semana 2**: Lecciones 03 (Definiendo los Datos) y 04 (Estadística y Probabilidad).
- **Semana 3**: Lecciones 05 (Bases de Datos Relacionales) y 06 (Bases de Datos NoSQL).
- **Semana 4**: Lecciones 07 (Python para Ciencia de Datos) y 08 (Preparación de Datos / Data Wrangling).
- **Semana 5**: Lecciones 09 (Visualización de Cantidades) y 10 (Visualización de Distribuciones).
- **Semana 6**: Lecciones 11 (Visualización de Proporciones) y 12 (Visualización de Relaciones).
- **Semana 7**: Lección 13 (Visualizaciones Significativas y Storytelling).
- **Semana 8**: Lecciones 14 (Ciclo de Vida de Ciencia de Datos) y 15 (Análisis y Modelado).
- **Semana 9**: Lecciones 16 (Comunicación de Resultados) y 17 (Introducción a la Nube).
- **Semana 10**: Lecciones 18/19 (Low-Code y Azure ML SDK) y 20 (Casos Reales y Presentación de Proyectos Finales).

### Opción B: Semestre Académico de 16 Semanas
Ideal para asignaturas de pregrado universitario (Ingeniería de Sistemas, Ciencia de la Computación, Economía, Estadística):

- **Semanas 1-2**: Fundamentos, qué es la disciplina y debate profundo sobre ética, sesgos y gobernanza de datos (Lecciones 01 y 02).
- **Semanas 3-4**: Taxonomía de datos, probabilidad y estadística inferencial aplicada (Lecciones 03 y 04).
- **Semanas 5-6**: Persistencia: SQL, álgebra relacional y modelos NoSQL (Lecciones 05 y 06).
- **Semanas 7-8**: Python analítico: NumPy, Pandas, manipulación, limpieza y tratamiento de valores atípicos y nulos (Lecciones 07 y 08).
- **Semana 9**: *Evaluación Parcial / Proyecto Intermedio de Análisis Exploratorio (EDA)*.
- **Semanas 10-12**: Visualización de datos, gramática de gráficos, buenas prácticas perceptivas y narrativa de datos (Lecciones 09 a 13).
- **Semanas 13-14**: Ciclo de vida metodológico (CRISP-DM / TDSP), modelado predictivo básico y comunicación técnica a audiencias de negocio (Lecciones 14 a 16).
- **Semana 15**: Ciencia de datos en la nube y herramientas MLOps (Lecciones 17 a 19).
- **Semana 16**: Lección 20 y Sustentación final de proyectos aplicados.

---

## Uso con GitHub Classroom

[GitHub Classroom](https://classroom.github.com/) simplifica de forma extraordinaria la gestión académica:

1. Crea una organización de GitHub para tu curso universitario o bootcamp.
2. Puedes dividir este repositorio por carpetas o permitir que cada alumno clone/forkee el repositorio completo.
3. Al crear una asignación en GitHub Classroom, los estudiantes recibirán automáticamente su propio repositorio privado con la tarea (`assignment.md` o `assignment.ipynb`).
4. Puedes integrar pruebas automáticas con GitHub Actions o calificar mediante *Pull Requests*, dejando comentarios formativos línea por línea en los cuadernos de Jupyter.

---

## Evaluación y Rúbricas Formativas

Recomendamos que la calificación de las tareas y proyectos no se base únicamente en que el código "corra sin errores", sino en la calidad integral del análisis. Sugerimos la siguiente rúbrica estándar (ponderación sobre 100 puntos):

| Criterio | Ponderación | Excelente (90-100%) | Aceptable (70-89%) | Necesita Mejora (<70%) |
|:---|:---:|:---|:---|:---|
| **Rigor y Corrección Técnica** | 35% | Código limpio, modular, uso óptimo de Pandas/NumPy, modelos bien validados. | El código funciona pero con redundancias o métodos ineficientes. | Errores de ejecución o métodos conceptualmente incorrectos. |
| **Interpretación y Análisis Crítico** | 30% | Explica con claridad qué significan las métricas y gráficos; deduce conclusiones sólidas. | Describe los números superficialmente sin explicar su impacto. | Omite el análisis escrito o incluye conclusiones ficticias/infundadas. |
| **Calidad de las Visualizaciones** | 20% | Gráficos autoexplicativos, con títulos, etiquetas de ejes, escalas apropiadas y paletas accesibles. | Gráficos correctos pero carentes de etiquetas o con sobrecarga visual. | Gráficos confusos, tipo de gráfico inadecuado para la variable analizada. |
| **Documentación y Reproducibilidad** | 15% | Celdas Markdown bien redactadas, estructura limpia, entorno reproducible. | Markdown escaso o código poco comentado. | Cuaderno desordenado, celdas ejecutadas fuera de orden secuencial. |

---

## Manejo de Dudas y Dinámicas de Aula

- **Fomentar el "Pair Programming" (Programación en Parejas)**: Para los laboratorios de Pandas y visualización, organizar a los estudiantes en parejas (uno como *driver* que teclea y otro como *navigator* que revisa la lógica) incrementa drásticamente la retención y disminuye la frustración por errores de sintaxis.
- **Salas de Trabajo para Debates Éticos (Lección 02)**: La lección de ética es una oportunidad extraordinaria para debates en grupo. Plantee casos reales de sesgo en selección de personal por IA o reconocimiento facial, y pida a los estudiantes redactar un código de conducta para su propio equipo de datos.
- **Uso de Datos Locales de América Latina**: Alentamos a los docentes a complementar las tareas con datasets abiertos de sus propios países (ej. datos de transporte público de Ciudad de México, datos epidemiológicos de Colombia, datos socioeconómicos de Argentina, Chile o Perú). Esto incrementa exponencialmente la relevancia y el compromiso del alumnado.

---

## Consideraciones Éticas y Pensamiento Crítico

Como docentes, recordemos siempre a nuestros estudiantes:

> *"Los datos no son la realidad en sí misma; son una representación cuantificada y potencialmente sesgada de ella. Nuestro deber ético es cuestionar los datos, verificar sus fuentes y construir modelos que promuevan la equidad, la transparencia y el bienestar social."*
