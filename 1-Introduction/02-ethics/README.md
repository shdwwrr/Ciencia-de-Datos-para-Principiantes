# Introducción a la Ética de los Datos

|![ Sketchnote por [(@sketchthedocs)](https://sketchthedocs.dev) ](../../sketchnotes/02-Ethics.png)|
|:---:|
| Ética en Ciencia de Datos - _Sketchnote por [@nitya](https://twitter.com/nitya)_ |

---

Todos somos ciudadanos de datos viviendo en un mundo dataficado.

Las tendencias del mercado indican que para 2022, 1 de cada 3 grandes organizaciones comprará y venderá sus datos a través de [mercados y plataformas de intercambio](https://www.gartner.com/smarterwithgartner/gartner-top-10-trends-in-data-and-analytics-for-2020/) en línea. Como **desarrolladores de aplicaciones**, será más fácil y económico integrar conocimientos basados en datos y automatización impulsada por algoritmos en las experiencias diarias de los usuarios. Pero a medida que la IA se vuelve omnipresente, también necesitaremos comprender los posibles daños causados por la [utilización indebida](https://www.youtube.com/watch?v=TQHs8SA1qpk) de estos algoritmos a gran escala.

Las tendencias sugieren que para 2025 generaremos y consumiremos más de [180 zettabytes](https://www.statista.com/statistics/871513/worldwide-data-created/) de datos. Para los **científicos de datos**, esta explosión de información proporciona un acceso sin precedentes a datos personales y de comportamiento. Con ello viene el poder de construir perfiles detallados de usuarios e influir sutilmente en la toma de decisiones, a menudo de maneras que fomentan una [ilusión de libre elección](https://www.datasciencecentral.com/the-pareto-set-and-the-paradox-of-choice/). Aunque esto puede usarse para orientar a los usuarios hacia resultados preferidos, también plantea preguntas críticas sobre la privacidad de los datos, la autonomía y los límites éticos de la influencia algorítmica.

La ética de los datos se ha convertido en _guías necesarias_ para la ciencia y la ingeniería de datos, ayudándonos a minimizar los posibles daños y consecuencias no deseadas de nuestras acciones impulsadas por datos. El [Ciclo de Hype de Gartner para IA](https://www.gartner.com/smarterwithgartner/2-megatrends-dominate-the-gartner-hype-cycle-for-artificial-intelligence-2020/) identifica tendencias relevantes en ética digital, IA responsable y gobernanza de IA como impulsores clave de megatendencias más amplias en torno a la _democratización_ y _industrialización_ de la IA.

![Ciclo de Hype de Gartner para IA - 2020](https://images-cdn.newscred.com/Zz1mOWJhNzlkNDA2ZTMxMWViYjRiOGFiM2IyMjQ1YmMwZQ==)

En esta lección, exploraremos el fascinante ámbito de la ética de los datos: desde conceptos básicos y desafíos, hasta estudios de caso y conceptos aplicados de IA como la gobernanza, que ayudan a establecer una cultura ética en equipos y organizaciones que trabajan con datos e IA.

## [Cuestionario previo a la clase](https://ff-quizzes.netlify.app/quiz/2?loc=es) 🎯

## Definiciones Básicas

Comencemos entendiendo la terminología básica.

La palabra "ética" proviene de la [palabra griega "ethikos"](https://en.wikipedia.org/wiki/Ethics) (y su raíz "ethos") que significa _carácter o naturaleza moral_.

**Ética** trata sobre los valores compartidos y principios morales que gobiernan nuestro comportamiento en la sociedad. La ética no se basa en leyes, sino en normas ampliamente aceptadas de lo que es "correcto vs. incorrecto". Sin embargo, las consideraciones éticas pueden influir en iniciativas de gobernanza corporativa y regulaciones gubernamentales que crean más incentivos para el cumplimiento.

**Ética de los Datos** es una [nueva rama de la ética](https://royalsocietypublishing.org/doi/full/10.1098/rsta.2016.0360#sec-1) que "estudia y evalúa problemas morales relacionados con _datos, algoritmos y prácticas correspondientes_". Aquí, **"datos"** se centra en acciones relacionadas con la generación, registro, curación, procesamiento, difusión, intercambio y uso; **"algoritmos"** se enfoca en IA, agentes, aprendizaje automático y robots; y **"prácticas"** aborda temas como innovación responsable, programación, hacking y códigos éticos.

**Ética Aplicada** es la [aplicación práctica de consideraciones morales](https://en.wikipedia.org/wiki/Applied_ethics). Es el proceso de investigar activamente cuestiones éticas en el contexto de _acciones, productos y procesos del mundo real_, y tomar medidas correctivas para garantizar que permanezcan alineados con nuestros valores éticos definidos.

**Cultura Ética** trata de [_operacionalizar_ la ética aplicada](https://hbr.org/2019/05/how-to-design-an-ethical-organization) para asegurarse de que nuestros principios y prácticas éticas sean adoptados de manera consistente y escalable en toda la organización. Las culturas éticas exitosas definen principios éticos a nivel organizacional, proporcionan incentivos significativos para el cumplimiento y refuerzan las normas éticas alentando y amplificando los comportamientos deseados en todos los niveles de la organización.

## Conceptos de Ética

En esta sección, discutiremos conceptos como **valores compartidos** (principios) y **desafíos éticos** (problemas) para la ética de los datos, y exploraremos **estudios de caso** que te ayudarán a entender estos conceptos en contextos del mundo real.

### 1. Principios Éticos

Toda estrategia de ética de los datos comienza definiendo _principios éticos_: los "valores compartidos" que describen comportamientos aceptables y guían acciones conformes en nuestros proyectos de datos e IA. Puedes definirlos a nivel individual o de equipo. Sin embargo, la mayoría de las grandes organizaciones los delinean en una declaración de misión o marco de _IA ética_ que se define a nivel corporativo y se aplica de manera consistente en todos los equipos.

**Ejemplo:** La declaración de misión de [IA Responsable](https://www.microsoft.com/en-us/ai/responsible-ai) de Microsoft dice: _"Estamos comprometidos con el avance de la IA impulsada por principios éticos que ponen a las personas primero"_, identificando 6 principios éticos en el marco a continuación:

![IA Responsable en Microsoft](https://docs.microsoft.com/en-gb/azure/cognitive-services/personalizer/media/ethics-and-responsible-use/ai-values-future-computed.png)

Exploremos brevemente estos principios. _Transparencia_ y _responsabilidad_ son valores fundamentales sobre los que se construyen otros principios, así que comencemos por ahí:

* [**Responsabilidad**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) hace que los profesionales sean _responsables_ de sus operaciones de datos e IA y del cumplimiento de estos principios éticos.
* [**Transparencia**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) asegura que las acciones de datos e IA sean _comprensibles_ (interpretables) para los usuarios, explicando el qué y el porqué detrás de las decisiones.
* [**Equidad**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1%3aprimaryr6) se centra en garantizar que la IA trate a _todas las personas_ de manera justa, abordando cualquier sesgo socio-técnico sistémico o implícito en los datos y sistemas.
* [**Fiabilidad y Seguridad**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) asegura que la IA se comporte de manera _consistente_ con los valores definidos, minimizando posibles daños o consecuencias no deseadas.
* [**Privacidad y Seguridad**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) trata de comprender el linaje de los datos y proporcionar _protecciones de privacidad de datos_ relacionadas a los usuarios.
* [**Inclusión**](https://www.microsoft.com/en-us/ai/responsible-ai?activetab=pivot1:primaryr6) trata de diseñar soluciones de IA con intención, adaptándolas para satisfacer una _amplia gama de necesidades y capacidades humanas_.

> 🚨 Piensa en cuál podría ser tu declaración de misión de ética de los datos. Explora marcos de IA ética de otras organizaciones: aquí hay ejemplos de [IBM](https://www.ibm.com/cloud/learn/ai-ethics), [Google](https://ai.google/principles) y [Facebook](https://ai.facebook.com/blog/facebooks-five-pillars-of-responsible-ai/). ¿Qué valores compartidos tienen en común? ¿Cómo se relacionan estos principios con el producto o la industria de IA en la que operan?

### 2. Desafíos Éticos

Una vez que hemos definido los principios éticos, el siguiente paso es evaluar nuestras acciones de datos e IA para ver si se alinean con esos valores compartidos. Piensa en tus acciones en dos categorías: _recolección de datos_ y _diseño de algoritmos_.

En la recolección de datos, las acciones probablemente involucrarán **datos personales** o información personalmente identificable (PII) de individuos identificables. Esto incluye [diversos elementos de datos no personales](https://ec.europa.eu/info/law/law-topic/data-protection/reform/what-personal-data_en) que _colectivamente_ identifican a un individuo. Los desafíos éticos pueden estar relacionados con la _privacidad de los datos_, la _propiedad de los datos_ y temas relacionados como el _consentimiento informado_ y los _derechos de propiedad intelectual_ de los usuarios.

En el diseño de algoritmos, las acciones implicarán recopilar y curar **conjuntos de datos**, luego utilizarlos para entrenar y desplegar **modelos de datos** que predigan resultados o automaticen decisiones en contextos del mundo real. Los desafíos éticos pueden surgir de _sesgos en los conjuntos de datos_, problemas de _calidad de los datos_, _injusticias_ y _representaciones erróneas_ en los algoritmos, incluyendo algunos problemas que son sistémicos por naturaleza.

En ambos casos, los desafíos éticos destacan áreas donde nuestras acciones pueden entrar en conflicto con nuestros valores compartidos. Para detectar, mitigar, minimizar o eliminar estas preocupaciones, necesitamos hacer preguntas morales de "sí/no" relacionadas con nuestras acciones y luego tomar medidas correctivas según sea necesario. Veamos algunos desafíos éticos y las preguntas morales que plantean:

#### 2.1 Propiedad de los Datos

La recolección de datos a menudo implica datos personales que pueden identificar a los sujetos de los datos. [La propiedad de los datos](https://permission.io/blog/data-ownership) trata sobre el _control_ y los [_derechos de los usuarios_](https://permission.io/blog/data-ownership) relacionados con la creación, procesamiento y difusión de datos.

Las preguntas morales que debemos hacer son:
 * ¿Quién posee los datos? (usuario u organización)
 * ¿Qué derechos tienen los sujetos de los datos? (ej.: acceso, eliminación, portabilidad)
 * ¿Qué derechos tienen las organizaciones? (ej.: rectificar reseñas maliciosas de usuarios)

#### 2.2 Consentimiento Informado

[El consentimiento informado](https://legaldictionary.net/informed-consent/) define el acto de que los usuarios acepten una acción (como la recolección de datos) con un _entendimiento completo_ de los hechos relevantes, incluyendo el propósito, los riesgos potenciales y las alternativas.

Preguntas para explorar aquí son:
 * ¿El usuario (sujeto de los datos) dio permiso para la captura y uso de datos?
 * ¿El usuario entendió el propósito para el cual se capturaron esos datos?
 * ¿El usuario entendió los riesgos potenciales de su participación?

#### 2.3 Propiedad Intelectual

[La propiedad intelectual](https://en.wikipedia.org/wiki/Intellectual_property) se refiere a creaciones intangibles resultantes de la iniciativa humana, que pueden _tener valor económico_ para individuos o empresas.

Preguntas para explorar aquí son:
 * ¿Los datos recopilados tienen valor económico para un usuario o empresa?
 * ¿El **usuario** tiene propiedad intelectual aquí?
 * ¿La **organización** tiene propiedad intelectual aquí?
 * Si existen estos derechos, ¿cómo los estamos protegiendo?

#### 2.4 Privacidad de los Datos

[La privacidad de los datos](https://www.northeastern.edu/graduate/blog/what-is-data-privacy/) o privacidad de la información se refiere a la preservación de la privacidad del usuario y la protección de su identidad con respecto a información personalmente identificable.

Preguntas para explorar aquí son:
 * ¿Los datos (personales) de los usuarios están protegidos contra hackeos y filtraciones?
 * ¿Los datos de los usuarios son accesibles solo para usuarios y contextos autorizados?
 * ¿Se preserva el anonimato de los usuarios cuando los datos se comparten o difunden?
 * ¿Se puede desidentificar a un usuario de conjuntos de datos anonimizados?

#### 2.5 Derecho al Olvido

El [Derecho al Olvido](https://en.wikipedia.org/wiki/Right_to_be_forgotten) o [Derecho de Eliminación](https://www.gdpreu.org/right-to-be-forgotten/) proporciona protección adicional de datos personales a los usuarios. Específicamente, da a los usuarios el derecho a solicitar la eliminación o eliminación de datos personales de búsquedas en Internet y otros lugares, _bajo circunstancias específicas_, permitiéndoles un nuevo comienzo en línea sin que se les juzgue por acciones pasadas.

Preguntas para explorar aquí son:
 * ¿El sistema permite a los sujetos de los datos solicitar la eliminación?
 * ¿Debería el retiro del consentimiento del usuario activar la eliminación automática?
 * ¿Se recopilaron datos sin consentimiento o por medios ilegales?
 * ¿Cumplimos con las regulaciones gubernamentales sobre privacidad de datos?

#### 2.6 Sesgo en los Conjuntos de Datos

El sesgo en los conjuntos de datos o [sesgo de recolección](http://researcharticles.com/index.php/bias-in-data-collection-in-research/) trata sobre seleccionar un subconjunto _no representativo_ de datos para el desarrollo de algoritmos, creando potencialmente resultados injustos para diversos grupos. Los tipos de sesgo incluyen sesgo de selección o muestreo, sesgo de voluntarios y sesgo de instrumentos.

Preguntas para explorar aquí son:
 * ¿Reclutamos un conjunto representativo de sujetos de datos?
 * ¿Probamos nuestro conjunto de datos recopilado o curado para diversos sesgos?
 * ¿Podemos mitigar o eliminar los sesgos descubiertos?

#### 2.7 Calidad de los Datos

[La calidad de los datos](https://lakefs.io/data-quality-testing/) analiza la validez del conjunto de datos curado utilizado para desarrollar nuestros algoritmos, verificando si las características y registros cumplen con los requisitos para el nivel de precisión y consistencia necesario para nuestro propósito de IA.

Preguntas para explorar aquí son:
 * ¿Capturamos características válidas para nuestro caso de uso?
 * ¿Se capturaron datos de manera _consistente_ en diversas fuentes de datos?
 * ¿Está el conjunto de datos _completo_ para diversas condiciones o escenarios?
 * ¿Se captura la información _con precisión_ reflejando la realidad?

#### 2.8 Justicia Algorítmica

[Justicia Algorítmica](https://towardsdatascience.com/what-is-algorithm-fairness-3182e161cf9f) evalúa si el diseño del algoritmo discrimina sistemáticamente contra subgrupos específicos de sujetos de datos, lo que puede llevar a [daños potenciales](https://docs.microsoft.com/en-us/azure/machine-learning/concept-fairness-ml) en la _asignación_ (donde se niegan o retienen recursos para ese grupo) y en la _calidad del servicio_ (donde la IA no es tan precisa para algunos subgrupos como lo es para otros).

Preguntas para explorar aquí:
 * ¿Evaluamos la precisión del modelo para diversos subgrupos y condiciones?
 * ¿Examinamos el sistema en busca de posibles daños (por ejemplo, estereotipos)?
 * ¿Podemos revisar los datos o reentrenar los modelos para mitigar los daños identificados?

Explora recursos como [listas de verificación de justicia en IA](https://query.prod.cms.rt.microsoft.com/cms/api/am/binary/RE4t6dA) para aprender más.

#### 2.9 Representación Errónea

[Representación Errónea de Datos](https://www.sciencedirect.com/topics/computer-science/misrepresentation) se trata de preguntar si estamos comunicando ideas basadas en datos reportados honestamente de manera engañosa para apoyar una narrativa deseada.

Preguntas para explorar aquí:
 * ¿Estamos reportando datos incompletos o inexactos?
 * ¿Estamos visualizando datos de manera que lleve a conclusiones engañosas?
 * ¿Estamos utilizando técnicas estadísticas selectivas para manipular resultados?
 * ¿Existen explicaciones alternativas que puedan ofrecer una conclusión diferente?

#### 2.10 Libre Elección
La [Ilusión de Libre Elección](https://www.datasciencecentral.com/profiles/blogs/the-illusion-of-choice) ocurre cuando las "arquitecturas de elección" del sistema utilizan algoritmos de toma de decisiones para influir a las personas hacia un resultado preferido mientras aparentan darles opciones y control. Estos [patrones oscuros](https://www.darkpatterns.org/) pueden causar daños sociales y económicos a los usuarios. Dado que las decisiones de los usuarios impactan los perfiles de comportamiento, estas acciones potencialmente impulsan elecciones futuras que pueden amplificar o extender el impacto de estos daños.

Preguntas para explorar aquí:
 * ¿El usuario entendió las implicaciones de tomar esa decisión?
 * ¿El usuario estaba al tanto de las opciones (alternativas) y los pros y contras de cada una?
 * ¿Puede el usuario revertir una elección automatizada o influenciada más tarde?

### 3. Estudios de Caso

Para contextualizar estos desafíos éticos en el mundo real, es útil observar estudios de caso que destacan los posibles daños y consecuencias para individuos y la sociedad cuando se pasan por alto estas violaciones éticas.

Aquí hay algunos ejemplos:

| Desafío Ético | Estudio de Caso  | 
|--- |--- |
| **Consentimiento Informado** | 1972 - [Estudio de Sífilis de Tuskegee](https://en.wikipedia.org/wiki/Tuskegee_Syphilis_Study) - A los hombres afroamericanos que participaron en el estudio se les prometió atención médica gratuita _pero fueron engañados_ por investigadores que no les informaron sobre su diagnóstico ni sobre la disponibilidad de tratamiento. Muchos murieron y sus parejas o hijos se vieron afectados; el estudio duró 40 años. | 
| **Privacidad de Datos** |  2007 - El [premio de datos de Netflix](https://www.wired.com/2007/12/why-anonymous-data-sometimes-isnt/) proporcionó a los investigadores _10M de clasificaciones de películas anonimizadas de 50K clientes_ para mejorar los algoritmos de recomendación. Sin embargo, los investigadores pudieron correlacionar datos anonimizados con datos personalmente identificables en _conjuntos de datos externos_ (por ejemplo, comentarios de IMDb), desanonimizando efectivamente a algunos suscriptores de Netflix.|
| **Sesgo en la Recolección**  | 2013 - La ciudad de Boston [desarrolló Street Bump](https://www.boston.gov/transportation/street-bump), una aplicación que permitía a los ciudadanos reportar baches, proporcionando a la ciudad mejores datos sobre carreteras para identificar y solucionar problemas. Sin embargo, [las personas de grupos de ingresos más bajos tenían menos acceso a autos y teléfonos](https://hbr.org/2013/04/the-hidden-biases-in-big-data), haciendo que sus problemas de carreteras fueran invisibles en esta aplicación. Los desarrolladores trabajaron con académicos para abordar _problemas de acceso equitativo y brechas digitales_ para mayor justicia. |
| **Justicia Algorítmica**  | 2018 - El MIT [Estudio Gender Shades](http://gendershades.org/overview.html) evaluó la precisión de productos de IA para clasificación de género, exponiendo brechas en precisión para mujeres y personas de color. Una [tarjeta de crédito de Apple en 2019](https://www.wired.com/story/the-apple-card-didnt-see-genderand-thats-the-problem/) parecía ofrecer menos crédito a mujeres que a hombres. Ambos casos ilustraron problemas de sesgo algorítmico que llevaron a daños socioeconómicos.|
| **Representación Errónea de Datos** | 2020 - El [Departamento de Salud Pública de Georgia publicó gráficos de COVID-19](https://www.vox.com/covid-19-coronavirus-us-response-trump/2020/5/18/21262265/georgia-covid-19-cases-declining-reopening) que parecían engañar a los ciudadanos sobre las tendencias de casos confirmados con un orden no cronológico en el eje x. Esto ilustra la representación errónea mediante trucos de visualización. |
| **Ilusión de Libre Elección** | 2020 - La aplicación educativa [ABCmouse pagó $10M para resolver una queja de la FTC](https://www.washingtonpost.com/business/2020/09/04/abcmouse-10-million-ftc-settlement/) donde los padres quedaron atrapados pagando suscripciones que no podían cancelar. Esto ilustra patrones oscuros en arquitecturas de elección, donde los usuarios fueron influenciados hacia elecciones potencialmente dañinas. |
| **Privacidad de Datos y Derechos de los Usuarios** | 2021 - La [brecha de datos de Facebook](https://www.npr.org/2021/04/09/986005820/after-data-breach-exposes-530-million-facebook-says-it-will-not-notify-users) expuso datos de 530M usuarios, resultando en un acuerdo de $5B con la FTC. Sin embargo, se negó a notificar a los usuarios sobre la brecha, violando los derechos de los usuarios en torno a la transparencia y el acceso a los datos. |

¿Quieres explorar más estudios de caso? Consulta estos recursos:
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) - dilemas éticos en diversas industrias. 
* [Curso de Ética en Ciencia de Datos](https://www.coursera.org/learn/data-science-ethics#syllabus) - estudios de caso emblemáticos explorados.
* [Dónde las cosas han salido mal](https://deon.drivendata.org/examples/) - lista de verificación de Deon con ejemplos.

> 🚨 Piensa en los estudios de caso que has visto: ¿has experimentado o te ha afectado un desafío ético similar en tu vida? ¿Puedes pensar en al menos un estudio de caso adicional que ilustre uno de los desafíos éticos que hemos discutido en esta sección?

## Ética Aplicada

Hemos hablado sobre conceptos éticos, desafíos y estudios de caso en contextos del mundo real. Pero, ¿cómo comenzamos a _aplicar_ principios y prácticas éticas en nuestros proyectos? ¿Y cómo _operacionalizamos_ estas prácticas para una mejor gobernanza? Exploremos algunas soluciones del mundo real:

### 1. Códigos Profesionales

Los Códigos Profesionales ofrecen una opción para que las organizaciones "incentiven" a sus miembros a apoyar sus principios éticos y declaración de misión. Los códigos son _directrices morales_ para el comportamiento profesional, ayudando a los empleados o miembros a tomar decisiones que se alineen con los principios de su organización. Solo son efectivos si los miembros cumplen voluntariamente; sin embargo, muchas organizaciones ofrecen recompensas y sanciones adicionales para motivar el cumplimiento.

Ejemplos incluyen:

 * [Oxford Munich](http://www.code-of-ethics.org/code-of-conduct/) Código de Ética
 * [Data Science Association](http://datascienceassn.org/code-of-conduct.html) Código de Conducta (creado en 2013)
 * [ACM Código de Ética y Conducta Profesional](https://www.acm.org/code-of-ethics) (desde 1993)

> 🚨 ¿Perteneces a una organización profesional de ingeniería o ciencia de datos? Explora su sitio para ver si definen un código profesional de ética. ¿Qué dice esto sobre sus principios éticos? ¿Cómo están "incentivando" a los miembros para seguir el código?

### 2. Listas de Verificación Éticas

Mientras que los códigos profesionales definen el _comportamiento ético_ requerido de los practicantes, [tienen limitaciones conocidas](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md) en su aplicación, particularmente en proyectos a gran escala. En cambio, muchos expertos en ciencia de datos [abogan por listas de verificación](https://resources.oreilly.com/examples/0636920203964/blob/master/of_oaths_and_checklists.md), que pueden **conectar principios con prácticas** de manera más determinista y accionable.

Las listas de verificación convierten preguntas en tareas de "sí/no" que pueden ser operacionalizadas, permitiendo que se rastreen como parte de los flujos de trabajo estándar de lanzamiento de productos.

Ejemplos incluyen:
 * [Deon](https://deon.drivendata.org/) - una lista de verificación de ética en datos de propósito general creada a partir de [recomendaciones de la industria](https://deon.drivendata.org/#checklist-citations) con una herramienta de línea de comandos para fácil integración.
 * [Lista de Verificación de Auditoría de Privacidad](https://cyber.harvard.edu/ecommerce/privacyaudit.html) - proporciona orientación general para prácticas de manejo de información desde perspectivas legales y sociales.
 * [Lista de Verificación de Justicia en IA](https://www.microsoft.com/en-us/research/project/ai-fairness-checklist/) - creada por practicantes de IA para apoyar la adopción e integración de controles de justicia en los ciclos de desarrollo de IA.
 * [22 preguntas para ética en datos e IA](https://medium.com/the-organization/22-questions-for-ethics-in-data-and-ai-efb68fd19429) - marco más abierto, estructurado para la exploración inicial de problemas éticos en diseño, implementación y contextos organizacionales.

### 3. Regulaciones Éticas

La ética trata de definir valores compartidos y hacer lo correcto _voluntariamente_. **Cumplimiento** trata de _seguir la ley_ si está definida. **Gobernanza** abarca todas las formas en que las organizaciones operan para hacer cumplir principios éticos y cumplir con las leyes establecidas.

Hoy en día, la gobernanza toma dos formas dentro de las organizaciones. Primero, se trata de definir principios de **IA ética** y establecer prácticas para operacionalizar la adopción en todos los proyectos relacionados con IA en la organización. Segundo, se trata de cumplir con todas las **regulaciones de protección de datos** impuestas por el gobierno en las regiones donde opera.

Ejemplos de regulaciones de protección de datos y privacidad:

 * `1974`, [Ley de Privacidad de EE.UU.](https://www.justice.gov/opcl/privacy-act-1974) - regula la recolección, uso y divulgación de información personal por parte del _gobierno federal_.
 * `1996`, [Ley de Portabilidad y Responsabilidad de Seguros de Salud de EE.UU. (HIPAA)](https://www.cdc.gov/phlp/publications/topic/hipaa.html) - protege datos personales de salud.
 * `1998`, [Ley de Protección de Privacidad en Línea para Niños de EE.UU. (COPPA)](https://www.ftc.gov/enforcement/rules/rulemaking-regulatory-reform-proceedings/childrens-online-privacy-protection-rule) - protege la privacidad de datos de niños menores de 13 años.
 * `2018`, [Reglamento General de Protección de Datos (GDPR)](https://gdpr-info.eu/) - proporciona derechos de usuario, protección de datos y privacidad.
 * `2018`, [Ley de Privacidad del Consumidor de California (CCPA)](https://www.oag.ca.gov/privacy/ccpa) otorga a los consumidores más _derechos_ sobre sus datos personales.
 * `2021`, [Ley de Protección de Información Personal de China](https://www.reuters.com/world/china/china-passes-new-personal-data-privacy-law-take-effect-nov-1-2021-08-20/) recién aprobada, creando una de las regulaciones de privacidad de datos en línea más fuertes a nivel mundial.

> 🚨 La Unión Europea definió el GDPR (Reglamento General de Protección de Datos), que sigue siendo una de las regulaciones de privacidad de datos más influyentes hoy en día. ¿Sabías que también define [8 derechos de usuario](https://www.freeprivacypolicy.com/blog/8-user-rights-gdpr) para proteger la privacidad digital y los datos personales de los ciudadanos? Aprende cuáles son y por qué importan.

### 4. Cultura Ética

Nota que sigue existiendo una brecha intangible entre el _cumplimiento_ (hacer lo suficiente para cumplir "la letra de la ley") y abordar [problemas sistémicos](https://www.coursera.org/learn/data-science-ethics/home/week/4) (como la osificación, la asimetría de información y la injusticia distributiva) que pueden acelerar la "armamentización" de la IA.

Esto último requiere [enfoques colaborativos para definir culturas éticas](https://towardsdatascience.com/why-ai-ethics-requires-a-culture-driven-approach-26f451afa29f) que construyan conexiones emocionales y valores compartidos consistentes _a través de organizaciones_ en la industria. Esto exige más [culturas éticas formalizadas en datos](https://www.codeforamerica.org/news/formalizing-an-ethical-data-culture/) en las organizaciones, permitiendo que _cualquiera_ [active el cordón Andon](https://en.wikipedia.org/wiki/Andon_(manufacturing)) (para plantear preocupaciones éticas temprano en el proceso) y haciendo que las _evaluaciones éticas_ (por ejemplo, en contrataciones) sean un criterio central en la formación de equipos para proyectos de IA.

---
## [Cuestionario post-lectura](https://ff-quizzes.netlify.app/quiz/3?loc=es) 🎯
## Revisión y Autoestudio 

Los cursos y libros ayudan a comprender los conceptos éticos fundamentales y los desafíos, mientras que los estudios de caso y herramientas ayudan con las prácticas éticas aplicadas en contextos del mundo real. Aquí hay algunos recursos para comenzar.
* [Machine Learning Para Principiantes](https://github.com/microsoft/ML-For-Beginners/blob/main/1-Introduction/3-fairness/README.md) - lección sobre Equidad, de Microsoft.  
* [Principios de IA Responsable](https://docs.microsoft.com/en-us/learn/modules/responsible-ai-principles/) - ruta de aprendizaje gratuita de Microsoft Learn.  
* [Ética y Ciencia de Datos](https://resources.oreilly.com/examples/0636920203964) - EBook de O'Reilly (M. Loukides, H. Mason et. al).  
* [Ética en Ciencia de Datos](https://www.coursera.org/learn/data-science-ethics#syllabus) - curso en línea de la Universidad de Michigan.  
* [Ethics Unwrapped](https://ethicsunwrapped.utexas.edu/case-studies) - estudios de caso de la Universidad de Texas.  

# Tarea  

[Escribe un Estudio de Caso sobre Ética de Datos](assignment.md)
