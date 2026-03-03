<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CONTENIDO SEMANA 12</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><hr>
<h1 id="teoría-de-sistemas-y-simulación---semana-12">TEORÍA DE SISTEMAS Y SIMULACIÓN - SEMANA 12</h1>
<h2 id="recapitulación-general-de-la-materia">RECAPITULACIÓN GENERAL DE LA MATERIA</h2>
<p>A lo largo de las once semanas anteriores, se ha desarrollado un recorrido completo y progresivo por los fundamentos, métodos y aplicaciones de la teoría de decisiones y la simulación de sistemas. Desde los conceptos básicos de la toma de decisiones bajo incertidumbre hasta la implementación práctica de modelos computacionales complejos, el curso ha proporcionado las herramientas conceptuales, analíticas y tecnológicas necesarias para abordar problemas del mundo real en ingeniería industrial, logística y cadena de suministro. Esta última semana está dedicada a la recapitulación y síntesis de todos los temas tratados, estableciendo conexiones entre ellos y reflexionando sobre su aplicación integrada en contextos profesionales.</p>
<p>*<strong>Conceptos clave de la recapitulación</strong></p>
<ul>
<li><strong>Integración conceptual:</strong> Comprensión de cómo los conceptos de las diferentes unidades se relacionan y complementan entre sí.</li>
<li><strong>Aplicación transversal:</strong> Identificación de cómo los métodos de decisión, simulación y modelación pueden aplicarse de manera combinada en problemas complejos.</li>
<li><strong>Visión sistémica:</strong> Capacidad para abordar problemas desde una perspectiva holística, considerando las interacciones entre componentes y niveles de decisión.</li>
<li><strong>Transferencia a la práctica:</strong> Reflexión sobre cómo los conocimientos adquiridos pueden transferirse a contextos profesionales reales.</li>
</ul>
<p>*<strong>Desarrollo del contenido</strong></p>
<h3 id="síntesis-de-las-unidades-temáticas">12.1 Síntesis de las Unidades Temáticas</h3>
<p>A continuación, se presenta una síntesis de cada una de las unidades y semanas del curso, estableciendo las conexiones fundamentales entre los conceptos y métodos estudiados.</p>
<h4 id="unidad-1-teoría-de-decisiones-semanas-1-2">Unidad 1: Teoría de Decisiones (Semanas 1-2)</h4>
<p><strong>Semana 1: Fundamentos conceptuales</strong><br>
Se establecieron las bases de la teoría de decisiones, incluyendo los elementos fundamentales de un problema de decisión (estados de la naturaleza, acciones y resultados), los tipos de entornos (determinista, riesgo, incierto y hostil) y los criterios para la toma de decisiones bajo incertidumbre (optimista, pesimista, Hurwicz, Laplace y Savage). La teoría general de sistemas se presentó como marco conceptual para entender las organizaciones como sistemas abiertos que interactúan con su entorno, enfatizando que las decisiones en una parte de la organización afectan al todo.</p>
<p><strong>Semana 2: Herramientas para la decisión</strong><br>
Se profundizó en la matriz de pagos como herramienta fundamental para representar problemas de decisión y en los árboles de decisión para modelar secuencias de decisiones y la incorporación de nueva información. El concepto de valor esperado y valor de la información perfecta proporcionó un puente hacia los entornos de riesgo y la cuantificación de la incertidumbre.</p>
<p><strong>Conexión con el resto del curso:</strong> Los conceptos de esta unidad son la base conceptual para todas las técnicas posteriores. La comprensión de los entornos de decisión y los criterios para elegir entre alternativas es fundamental para interpretar los resultados de los modelos de simulación y para diseñar experimentos que comparen diferentes escenarios.</p>
<h4 id="unidad-2-líneas-de-espera-teoría-de-colas-semanas-3-4">Unidad 2: Líneas de Espera (Teoría de Colas) (Semanas 3-4)</h4>
<p><strong>Semana 3: Fundamentos de sistemas de colas</strong><br>
Se introdujeron los conceptos básicos de los sistemas de líneas de espera, incluyendo la estructura general (fuente de entrada, proceso de llegada, mecanismo de servicio), la notación de Kendall para clasificar sistemas (A/B/c/k) y la Ley de Little (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>L</mi><mo>=</mo><mi>λ</mi><mi>W</mi></mrow><annotation encoding="application/x-tex">L = \lambda W</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathnormal">L</span><span class="mspace" style="margin-right: 0.277778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right: 0.277778em;"></span></span><span class="base"><span class="strut" style="height: 0.69444em; vertical-align: 0em;"></span><span class="mord mathnormal" style="margin-right: 0.13889em;">λW</span></span></span></span></span>) como relación fundamental independiente de las distribuciones subyacentes. Se presentó el marco de los procesos de nacimiento y muerte para modelar la evolución estocástica del número de clientes en el sistema.</p>
<p><strong>Semana 4: Modelos markovianos M/M/</strong>*<br>
Se desarrollaron los modelos analíticos más importantes de la teoría de colas: M/M/1 (un servidor), M/M/c (múltiples servidores), M/M/∞ (infinitos servidores) y M/M/c/k (capacidad finita). Se estableció la relación fundamental entre las distribuciones de Poisson y Exponencial, y se derivaron las ecuaciones para calcular las medidas de rendimiento clave (L, Lq, W, Wq).</p>
<p><strong>Conexión con el resto del curso:</strong> Estos modelos analíticos representan la primera aproximación cuantitativa al estudio de sistemas con incertidumbre. Sin embargo, sus limitaciones (supuestos de exponencialidad, homogeneidad, estado estacionario) motivan la necesidad de la simulación, que se aborda en las unidades siguientes. Los conceptos de tasa de llegada (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>λ</mi></mrow><annotation encoding="application/x-tex">\lambda</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.69444em; vertical-align: 0em;"></span><span class="mord mathnormal">λ</span></span></span></span></span>), tasa de servicio (<span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>μ</mi></mrow><annotation encoding="application/x-tex">\mu</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.625em; vertical-align: -0.19444em;"></span><span class="mord mathnormal">μ</span></span></span></span></span>) y medidas de rendimiento serán retomados en los modelos de simulación.</p>
<h4 id="unidad-3-simulación-y-generación-de-variables-aleatorias-semanas-5-6">Unidad 3: Simulación y Generación de Variables Aleatorias (Semanas 5-6)</h4>
<p><strong>Semana 5: Metodología de simulación y números aleatorios</strong><br>
Se presentó la simulación como metodología para el análisis de sistemas complejos cuando los modelos analíticos son insuficientes. Se introdujo el proceso estructurado de un estudio de simulación (formulación del problema, conceptualización, recolección de datos, construcción del modelo, verificación, validación, diseño de experimentos, ejecución y análisis). Se explicaron los fundamentos de los números pseudoaleatorios y el generador congruencial lineal como mecanismo de producción.</p>
<p><strong>Semana 6: Pruebas estadísticas y generación de variables aleatorias</strong><br>
Se abordó la validación estadística de los generadores de números aleatorios mediante pruebas de uniformidad (Chi-cuadrada, Kolmogorov-Smirnov) e independencia (correlación serial, pruebas de corridas). Se presentaron los métodos para generar variables aleatorias que sigan distribuciones específicas (transformada inversa, Box-Müller, aceptación-rechazo, búsqueda en tabla) a partir de números uniformes.</p>
<p><strong>Conexión con el resto del curso:</strong> Esta unidad proporciona las herramientas técnicas fundamentales para cualquier simulación estocástica. Los métodos de generación de variables aleatorias serán aplicados tanto en las simulaciones Montecarlo (Unidad 4) como en las simulaciones de eventos discretos (Unidad 5). Las pruebas de bondad de ajuste son esenciales para validar que las distribuciones utilizadas en los modelos representan adecuadamente los datos reales.</p>
<h4 id="unidad-4-método-montecarlo-semanas-7-8">Unidad 4: Método Montecarlo (Semanas 7-8)</h4>
<p><strong>Semana 7: Principios y distribuciones</strong><br>
Se introdujo el método Montecarlo como técnica de simulación estática para cuantificar el riesgo y la incertidumbre. Se presentaron las distribuciones de probabilidad más comunes (uniforme, triangular, normal, exponencial, lognormal, Poisson, binomial) y los métodos para generar muestras de las mismas. Se estableció la relación entre el método Montecarlo y la simulación en general.</p>
<p><strong>Semana 8: Aplicación y análisis de escenarios</strong><br>
Se desarrollaron ejemplos prácticos de simulación Montecarlo en contextos de logística, inventarios y evaluación de proyectos (VAN). Se introdujo el concepto de validación de modelos y los pasos estructurados para desarrollar una simulación Montecarlo. Se presentaron las técnicas para la comparación de escenarios, incluyendo el uso de números aleatorios comunes, la visualización con diagramas de caja y la interpretación de resultados para la toma de decisiones.</p>
<p><strong>Conexión con el resto del curso:</strong> El método Montecarlo integra los conceptos de probabilidad y generación de variables aleatorias (Unidad 3) con los criterios de decisión bajo riesgo (Unidad 1). Los resultados de las simulaciones Montecarlo (distribuciones de probabilidad de variables de salida) proporcionan información cuantitativa sobre el riesgo que puede ser utilizada en árboles de decisión para evaluar alternativas.</p>
<h4 id="unidad-5-modelación-discreta-de-sistemas-semanas-9-11">Unidad 5: Modelación Discreta de Sistemas (Semanas 9-11)</h4>
<p><strong>Semana 9: Lenguajes de simulación y modelos conceptuales</strong><br>
Se introdujo el formalismo DEVS como lenguaje para describir sistemas de eventos discretos, definiendo sus elementos fundamentales (estados, entradas, salidas, funciones de transición). Se abordó la construcción de modelos conceptuales mediante diagramas de flujo, diagramas de ciclo de actividades y diagramas de bloques, utilizando como referencia el caso de estudio de la planta de Cambay.</p>
<p><strong>Semana 10: Análisis de resultados y mejora de procesos</strong><br>
Se presentaron las técnicas estadísticas para analizar los resultados de simulaciones de eventos discretos, incluyendo el método de réplicas independientes, la construcción de intervalos de confianza y la importancia de eliminar el período transitorio. A través del caso de Cambay, se ilustró el ciclo completo de mejora basado en simulación: diagnóstico de cuellos de botella, formulación y evaluación de alternativas, y toma de decisiones informada.</p>
<p><strong>Semana 11: Implementación en software de simulación</strong><br>
Se profundizó en la construcción de modelos computacionales en AnyLogic, diferenciando entre estructura estática (recursos, layout) y estructura dinámica (flujo de entidades, lógica de eventos). Se presentaron los elementos básicos y avanzados del paquete de simulación (bloques <code>Seize</code>, <code>Delay</code>, <code>Release</code>, <code>SelectOutput</code>, <code>Hold</code>) y los comandos en Java para personalizar el comportamiento del modelo. El caso de Cambay sirvió como hilo conductor para todos los ejemplos.</p>
<p><strong>Conexión con el resto del curso:</strong> La modelación discreta de sistemas integra todos los conceptos previos: la definición de entidades, atributos y reglas de operación (Unidad 1), los conceptos de colas y teoría de líneas de espera (Unidad 2), la generación de variables aleatorias (Unidad 3) y el análisis de escenarios (Unidad 4). Los modelos de simulación de eventos discretos representan la herramienta más completa y flexible para el análisis de sistemas complejos, permitiendo superar las limitaciones de los modelos analíticos.</p>
<h3 id="aplicación-de-conceptos-en-la-literatura-académica-lecturas-sugeridas">12.2 Aplicación de Conceptos en la Literatura Académica (Lecturas Sugeridas)</h3>
<p>A lo largo del curso, se han sugerido diversos artículos académicos para ilustrar la aplicación de los conceptos y métodos presentados en estudios reales. A continuación, se presenta una guía que relaciona los temas de cada semana con ejemplos concretos de su uso en contextos de investigación aplicada. Se recomienda consultar estos estudios para una comprensión más profunda de cómo las herramientas analizadas en el curso se utilizan para resolver problemas complejos.</p>
<h4 id="semanas-1-2-teoría-de-decisiones-y-herramientas-de-decisión">Semanas 1-2: Teoría de Decisiones y Herramientas de Decisión</h4>
<p><strong>Lectura sugerida:</strong> Ghasemi et al. (2024) - “Simulation optimization applied to production scheduling in the era of industry 4.0: A review and future roadmap”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
Este artículo de revisión aborda la programación de la producción (production scheduling) como un problema de decisión fundamental en los sistemas de manufactura. El estudio presenta un marco conceptual que distingue tres niveles jerárquicos de decisión (estratégico, táctico y operacional), lo que refleja directamente los conceptos de la Unidad 1 sobre entornos de decisión y la teoría general de sistemas. El artículo enfatiza que las decisiones de programación tienen efectos horizontales y verticales en la organización, una visión sistémica clave presentada en la Semana 1. Además, los autores discuten la importancia de considerar la incertidumbre (tiempos de proceso, disponibilidad de máquinas, demanda) en los problemas de decisión, conectando con los conceptos de entornos de riesgo e incertidumbre. Es un excelente punto de partida para entender el estado del arte en la optimización de decisiones bajo incertidumbre.</p>
<h4 id="semanas-3-4-líneas-de-espera-y-modelos-markovianos">Semanas 3-4: Líneas de Espera y Modelos Markovianos</h4>
<p><strong>Lectura sugerida:</strong> Zhang et al. (2022) - “Research on Design Optimization of Subway Station Transfer Entrance Based on AnyLogic”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
Este estudio aplica simulación para analizar y optimizar el flujo de pasajeros en una estación de metro, un problema clásico de líneas de espera. Aunque no utiliza directamente los modelos analíticos M/M/*, los conceptos fundamentales de la teoría de colas están presentes en su análisis. El estudio mide la densidad regional (análoga a la longitud de la cola), la velocidad media del flujo de pasajeros (relacionada con el tiempo de servicio) y el tiempo de distribución de entrada y salida (tiempo en el sistema). Estos indicadores corresponden directamente a las medidas de rendimiento L, W y Lq. La investigación demuestra cómo los principios de la teoría de colas se aplican en la práctica para diagnosticar congestiones y proponer mejoras en el diseño de estaciones.</p>
<h4 id="semanas-5-6-simulación-y-generación-de-variables-aleatorias">Semanas 5-6: Simulación y Generación de Variables Aleatorias</h4>
<p><strong>Lectura sugerida:</strong> Ghasemi et al. (2024) - “Simulation optimization applied to production scheduling…”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
El artículo de Ghasemi et al. dedica una sección importante a analizar las fuentes de incertidumbre en los sistemas de producción, incluyendo tiempos de proceso estocásticos (PT), disponibilidad de máquinas (MAV), fechas de entrega (DD), tiempos de preparación (SetT) y demanda (Dem). Esto se relaciona directamente con la necesidad de generar variables aleatorias para modelar estas incertidumbres, un tema central de la Semana 6. El artículo también discute las pruebas de validación utilizadas en la literatura, como la comparación con casos de estudio y pruebas estadísticas, lo que refleja la importancia de la verificación y validación presentada en la Semana 5.</p>
<h4 id="semanas-7-8-método-montecarlo">Semanas 7-8: Método Montecarlo</h4>
<p><strong>Lectura sugerida:</strong> Maheshwari et al. (2023) - “Digital twin-driven real-time planning, monitoring, and controlling in food supply chains”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
Este estudio desarrolla un gemelo digital para una planta de procesamiento de alimentos (fabricación de helados). Si bien el método Montecarlo no es el enfoque principal, los autores utilizan la simulación para analizar el riesgo y la incertidumbre en la cadena de suministro. El estudio evalúa indicadores clave de rendimiento (tiempos de ciclo, utilización de equipos) afectados por la variabilidad inherente a los procesos. La simulación permite cuantificar la distribución de estos indicadores, lo que constituye una aplicación práctica del método Montecarlo en el contexto de la planificación de la producción bajo incertidumbre.</p>
<h4 id="semanas-9-11-modelación-discreta-de-sistemas-y-simulación-en-anylogic">Semanas 9-11: Modelación Discreta de Sistemas y Simulación en AnyLogic</h4>
<p><strong>Lectura sugerida 1:</strong> Zhang et al. (2022) - “Research on Design Optimization of Subway Station Transfer Entrance Based on AnyLogic”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
Este artículo es un excelente ejemplo de aplicación de la simulación de eventos discretos utilizando AnyLogic. Los autores construyen un modelo de la estación JieDaoKou del metro de Wuhan para analizar el flujo de pasajeros. El estudio demuestra los conceptos de la <strong>Semana 9</strong> sobre construcción de modelos conceptuales y su implementación computacional en AnyLogic. Utilizan elementos básicos del software para modelar el comportamiento de los pasajeros. El análisis de resultados se centra en la densidad regional (mapas de calor), el tiempo de entrada/salida y la velocidad media del flujo, reflejando las técnicas de la <strong>Semana 10</strong>. Finalmente, el estudio propone y evalúa tres escenarios de optimización (conectando con la <strong>Semana 8</strong>), demostrando el ciclo completo de mejora basado en simulación.</p>
<p><strong>Lectura sugerida 2:</strong> Maheshwari et al. (2023) - “Digital twin-driven real-time planning, monitoring, and controlling in food supply chains”</p>
<p><strong>Aplicación de conceptos (¿Qué se puede encontrar en este estudio?):</strong><br>
Este estudio constituye una aplicación avanzada de los conceptos de modelación discreta de sistemas utilizando AnyLogic, integrando múltiples temas del curso:</p>
<ul>
<li><strong>Semana 9:</strong> Los autores desarrollan un modelo conceptual detallado de la planta, identificando entidades, recursos y reglas de operación.</li>
<li><strong>Semana 10:</strong> Evalúan múltiples indicadores de rendimiento (tiempo de ciclo, utilización de equipos, nivel de servicio) para comparar el rendimiento de diferentes estrategias.</li>
<li><strong>Semana 11:</strong> La implementación en AnyLogic es el núcleo del estudio. Crean un gemelo digital que integra la estructura estática (equipos), la estructura dinámica (flujo de materiales), agentes (proveedores, planta, distribuidores) y datos en tiempo real. Este es un ejemplo de cómo llevar la simulación a un nivel de integración y aplicación industrial concreta.</li>
</ul>
<h4 id="síntesis-de-aplicaciones">Síntesis de Aplicaciones</h4>

<table>
<thead>
<tr>
<th align="left">Concepto</th>
<th align="left">Zhang et al. (2022)</th>
<th align="left">Maheshwari et al. (2023)</th>
<th align="left">Ghasemi et al. (2024)</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">Teoría de decisiones</td>
<td align="left">Identificación de alternativas de diseño</td>
<td align="left">Decisiones de aprovisionamiento, producción y distribución</td>
<td align="left">Niveles jerárquicos de decisión en manufactura</td>
</tr>
<tr>
<td align="left">Líneas de espera</td>
<td align="left">Densidad regional, tiempo de flujo, velocidad media</td>
<td align="left">Tiempo de ciclo, backlog, nivel de servicio</td>
<td align="left">Revisión de modelos de colas en programación de producción</td>
</tr>
<tr>
<td align="left">Simulación y vars. aleatorias</td>
<td align="left">Velocidad de pasajeros como variable aleatoria</td>
<td align="left">Tiempos de proceso y demanda como variables estocásticas</td>
<td align="left">Fuentes de incertidumbre en sistemas de producción</td>
</tr>
<tr>
<td align="left">Método Montecarlo</td>
<td align="left">Análisis de escenarios de diseño</td>
<td align="left">Evaluación de riesgo en cadena de suministro</td>
<td align="left">Optimización bajo incertidumbre</td>
</tr>
<tr>
<td align="left">Modelación discreta (AnyLogic)</td>
<td align="left">Implementación completa del modelo</td>
<td align="left">Gemelo digital con agentes y MILP</td>
<td align="left">No aplica (artículo de revisión)</td>
</tr>
</tbody>
</table><p>*<strong>Ejemplos de aplicación integrada</strong></p>
<p><strong>Ejemplo 1 (Manufactura):</strong> Una empresa manufacturera enfrenta el problema de decidir la capacidad óptima de producción (Semana 1). Utiliza un árbol de decisión para evaluar alternativas (ampliar planta, subcontratar, mantener capacidad actual) considerando la incertidumbre en la demanda (Semana 2). Recolecta datos históricos y determina que los tiempos de proceso siguen una distribución lognormal (Semana 6). Desarrolla un modelo de simulación de eventos discretos en AnyLogic (Semana 11) que incorpora líneas de espera en las estaciones de trabajo (Semana 3) y utiliza el método Montecarlo para analizar el riesgo de cada alternativa (Semana 8). Los resultados de la simulación proporcionan la distribución del VAN para cada escenario, informando la decisión final.</p>
<p><strong>Ejemplo 2 (Logística):</strong> Un centro de distribución debe decidir el número óptimo de muelles de carga (Semana 1). Utiliza un modelo M/M/c (Semana 4) para obtener una primera aproximación. Sin embargo, debido a la complejidad del sistema, desarrolla un modelo de simulación en AnyLogic (Semana 11) que incorpora la generación de variables aleatorias para los tiempos de llegada y servicio (Semana 6). Realiza múltiples réplicas (Semana 10) para obtener intervalos de confianza para el tiempo medio de espera y utiliza análisis de escenarios (Semana 8) para comparar configuraciones.</p>
<p><strong>Ejemplo 3 (Cadena de Suministro):</strong> Una empresa evalúa el riesgo de una inversión en una nueva instalación (Semana 1). Desarrolla un modelo de simulación Montecarlo (Semana 8) que incorpora la incertidumbre en la demanda, los precios de las materias primas y los tipos de cambio, modelados con distribuciones de probabilidad adecuadas (Semana 7). Los resultados de la simulación (distribución del VAN) se utilizan en un árbol de decisión para evaluar la opción de realizar un estudio de mercado adicional (valor de la información perfecta) (Semana 2).</p>
<p>*<strong>Cierre y Reflexión Final</strong></p>
<p>A lo largo de este curso, se ha construido un marco conceptual y metodológico integral para la toma de decisiones en sistemas complejos, caracterizados por la incertidumbre y la interacción dinámica de múltiples elementos. Se ha transitado desde los fundamentos teóricos de la decisión hasta la implementación práctica de modelos computacionales avanzados.</p>
<p>La integración de estos conocimientos permite abordar problemas del mundo real con una visión sistémica, utilizando las herramientas más adecuadas para cada nivel de análisis. Las lecturas sugeridas demuestran que estas técnicas no son solo ejercicios teóricos, sino herramientas poderosas que se aplican en la investigación y la práctica profesional para mejorar el rendimiento de sistemas industriales, logísticos y de servicios.</p>
<p>La competencia fundamental desarrollada es la capacidad de <strong>modelar</strong>: abstraer la realidad en una representación formal que capture los elementos esenciales del problema, seleccionar las herramientas apropiadas, implementar el modelo computacionalmente, analizar los resultados con rigor y traducirlos en recomendaciones accionables para la toma de decisiones. Esta competencia constituye una base sólida para enfrentar los desafíos de la industria 4.0 y la transformación digital de las organizaciones.</p>
<p>*<strong>Información complementaria</strong></p>
<p>Para profundizar en los temas tratados en el curso y explorar aplicaciones avanzadas, se recomienda consultar:</p>
<ol>
<li><strong>Law, A. M. (2015).</strong> <em>Simulation Modeling and Analysis</em> (5th ed.). McGraw-Hill.</li>
<li><strong>Banks, J., Carson, J. S., Nelson, B. L., &amp; Nicol, D. M. (2014).</strong> <em>Discrete-Event System Simulation</em> (5th ed.). Pearson.</li>
<li><strong>Pidd, M. (2004).</strong> <em>Computer Simulation in Management Science</em> (5th ed.). Wiley.</li>
<li><strong>Hillier, F. S., &amp; Lieberman, G. J. (2021).</strong> <em>Introducción a la Investigación de Operaciones</em> (11a ed.). McGraw-Hill.</li>
<li><strong>Repositorio de artículos:</strong> Los artículos analizados en esta semana (Zhang et al., 2022; Maheshwari et al., 2023; Ghasemi et al., 2024) están disponibles en bases de datos como ScienceDirect y constituyen excelentes ejemplos de aplicación de los conceptos del curso.</li>
</ol>
<p>*<strong>Referencias</strong></p>
<p>Ghasemi, A., Farajzadeh, F., Heavey, C., Fowler, J., &amp; Papadopoulos, C. T. (2024). Simulation optimization applied to production scheduling in the era of industry 4.0: A review and future roadmap. <em>Journal of Industrial Information Integration</em>, 39, 100599.</p>
<p>Maheshwari, P., Kamble, S., Belhadi, A., Venkatesh, M., &amp; Abedin, M. Z. (2023). Digital twin-driven real-time planning, monitoring, and controlling in food supply chains. <em>Technological Forecasting and Social Change</em>, 195, 122799.</p>
<p>Zhang, L., Li, M., &amp; Wang, Y. (2022). Research on design optimization of subway station transfer entrance based on AnyLogic. <em>7th International Conference on Intelligent, Interactive Systems and Applications</em>. Elsevier B.V.</p>
</div>
</body>

</html>
