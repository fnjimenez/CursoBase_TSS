<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CONTENIDO SEMANA 8</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><hr>
<h1 id="tteoría-de-sistemas-y-simulación---semana-8">TTEORÍA DE SISTEMAS Y SIMULACIÓN - SEMANA 8</h1>
<h2 id="unidad-4-método-montecarlo-continuación">UNIDAD 4: MÉTODO MONTECARLO (Continuación)</h2>
<p>En la semana anterior se establecieron los fundamentos del método Montecarlo, incluyendo los principios básicos, las distribuciones de probabilidad más comunes y los métodos para generar las muestras correspondientes. Con estas bases, se está en condiciones de abordar la aplicación práctica de la técnica. Esta semana se centra en el proceso completo de un estudio de simulación Montecarlo: desde la validación de los modelos estadísticos subyacentes, pasando por los pasos estructurados para desarrollar una simulación, hasta la comparación de escenarios alternativos para apoyar la toma de decisiones. Se presentarán ejemplos concretos en las áreas de logística, inventarios y evaluación de proyectos, demostrando cómo el método Montecarlo permite cuantificar el riesgo y la incertidumbre de manera rigurosa.</p>
<p><img src="image.png?conceptos_clave" alt=""> <em><strong>Conceptos clave</strong></em></p>
<ul>
<li><strong>Validación de modelos:</strong> Proceso de determinar si un modelo es una representación suficientemente precisa del sistema real para los propósitos del estudio.</li>
<li><strong>Simulación Montecarlo:</strong> Técnica que utiliza muestreo aleatorio repetido para obtener la distribución de probabilidad de una variable de salida en función de la incertidumbre de las variables de entrada.</li>
<li><strong>Escenario:</strong> Configuración específica de los parámetros de entrada de un modelo (ej. diferentes niveles de capacidad, distintas políticas de inventario).</li>
<li><strong>Análisis de escenarios:</strong> Comparación de los resultados de la simulación para diferentes configuraciones del sistema, con el fin de identificar la alternativa que ofrece el mejor equilibrio entre rendimiento y riesgo.</li>
<li><strong>Variable de respuesta:</strong> Medida de rendimiento de interés que se obtiene de la simulación (ej. costo total, nivel de servicio, tiempo de ciclo, VAN).</li>
</ul>
<p><img src="image.png?contenido" alt=""> *<strong>Desarrollo del contenido</strong></p>
<h3 id="validación-de-modelos-estadísticos">4.3 Validación de Modelos Estadísticos</h3>
<p>Un paso crítico antes de utilizar cualquier modelo para la toma de decisiones es asegurar que representa adecuadamente la realidad. La <strong>validación</strong> es el proceso de determinar si un modelo es una representación suficientemente precisa del sistema real para los propósitos del estudio (Rubinstein &amp; Kroese, 2016, p. 229). No se busca una réplica perfecta, sino un modelo lo suficientemente bueno para tomar decisiones correctas.</p>
<p>Las técnicas de validación incluyen:</p>
<ul>
<li>
<p><strong>Comparación con sistemas reales:</strong> Si el sistema real existe (aunque sea en una versión piloto), se comparan las salidas de la simulación con los datos observados del sistema. Se pueden usar pruebas estadísticas como la prueba t de Student para comparar medias o la prueba de Kolmogorov-Smirnov para comparar distribuciones enteras (Shonkwiler &amp; Mendivil, 2024, p. 219).</p>
</li>
<li>
<p><strong>Análisis de sensibilidad:</strong> Se examina cómo cambia la salida del modelo ante cambios pequeños en los parámetros de entrada. Si el modelo reacciona de manera plausible (por ejemplo, el VAN disminuye si aumentan los costos), es una señal positiva. Si es demasiado sensible a una variable que en la realidad es estable, puede haber un problema (Rubinstein &amp; Kroese, 2016, p. 238).</p>
</li>
<li>
<p><strong>Validación de supuestos:</strong> Se verifica que los supuestos distribucionales sobre las variables de entrada sean correctos, por ejemplo, usando pruebas de bondad de ajuste (chi-cuadrada, Kolmogorov-Smirnov) para confirmar que los datos históricos realmente siguen la distribución que se les ha asignado (Stevens, 2024, p. 189).</p>
</li>
<li>
<p><strong>Evaluación por expertos:</strong> Presentar la estructura y los resultados del modelo a expertos en el dominio del problema para que juzguen si el comportamiento del modelo tiene sentido desde una perspectiva cualitativa.</p>
</li>
</ul>
<h3 id="pasos-para-desarrollar-simulaciones-en-el-método-montecarlo">4.4 Pasos para Desarrollar Simulaciones en el Método Montecarlo</h3>
<p>A partir de los conceptos de Stevens (2024), el desarrollo de una simulación Monte Carlo sigue una secuencia lógica de pasos, desde la definición del problema hasta la implementación computacional.</p>
<ol>
<li>
<p><strong>Definir el problema y el objetivo:</strong> Establecer claramente la pregunta que se quiere responder. Por ejemplo, “¿Cuál es la probabilidad de que el proyecto X se complete en menos de 100 días?” o “¿Cuál es el nivel de inventario de seguridad que minimiza el costo total esperado?”.</p>
</li>
<li>
<p><strong>Identificar las variables de entrada inciertas:</strong> Listar todas las variables del modelo cuyo valor no se conoce con certeza. Para cada una, se debe determinar la distribución de probabilidad que mejor la representa (Uniforme, Normal, Exponencial, etc.) basándose en datos históricos o en el juicio de expertos (Stevens, 2024, p. 22).</p>
</li>
<li>
<p><strong>Construir el modelo matemático o lógico:</strong> Desarrollar las relaciones (ecuaciones o reglas lógicas) que conectan las variables de entrada con la variable de salida de interés (el objetivo). Para el VAN, sería la fórmula financiera. Para un proyecto, sería la red de precedencias.</p>
</li>
<li>
<p><strong>Implementar el modelo computacional:</strong> Escribir el código (en Python, R, Matlab, Excel, etc.) que toma una muestra de las variables de entrada, ejecuta el modelo y devuelve un resultado. Este código debe poder repetirse un gran número de veces de forma automática (Shonkwiler &amp; Mendivil, 2024, p. 4).</p>
</li>
<li>
<p><strong>Generar las muestras aleatorias:</strong> Utilizar un generador de números aleatorios y las técnicas de transformación (inversa, Box-Müller, etc.) para crear un gran número <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>N</mi></mrow><annotation encoding="application/x-tex">N</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span></span></span></span></span> (ej. 10,000) de conjuntos de valores de entrada plausibles.</p>
</li>
<li>
<p><strong>Ejecutar la simulación:</strong> Ejecutar el modelo computacional para cada uno de los <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>N</mi></mrow><annotation encoding="application/x-tex">N</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span></span></span></span></span> conjuntos de entrada. Esto generará <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>N</mi></mrow><annotation encoding="application/x-tex">N</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span></span></span></span></span> resultados diferentes, uno para cada escenario posible.</p>
</li>
<li>
<p><strong>Analizar los resultados:</strong> Los <span class="katex--inline"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>N</mi></mrow><annotation encoding="application/x-tex">N</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height: 0.68333em; vertical-align: 0em;"></span><span class="mord mathnormal" style="margin-right: 0.10903em;">N</span></span></span></span></span> resultados se analizan estadísticamente. Se calculan medidas como la media, la mediana, la desviación estándar y, crucialmente, se construyen histogramas o funciones de distribución acumulada para visualizar la incertidumbre (Stevens, 2024, p. 58). También se calculan intervalos de confianza para las estimaciones.</p>
</li>
</ol>
<h3 id="comparación-de-escenarios-simulados">4.5 Comparación de Escenarios Simulados</h3>
<p>El objetivo final de muchas simulaciones Monte Carlo es comparar el desempeño de diferentes diseños, políticas o escenarios para apoyar la toma de decisiones. Esta comparación va más allá de mirar los promedios.</p>
<ol>
<li>
<p><strong>Definir los escenarios:</strong> Identificar claramente las alternativas a comparar. Por ejemplo, “Política de inventario A (pedir 100 unidades cuando el stock llegue a 20)” vs. “Política B (pedir 150 unidades cuando el stock llegue a 30)”.</p>
</li>
<li>
<p><strong>Ejecutar la simulación para cada escenario:</strong> Utilizando las <strong>mismas secuencias de números aleatorios</strong> para todos los escenarios. Esta técnica, conocida como <strong>números aleatorios comunes</strong> (o <em>common random numbers</em>), es una poderosa técnica de reducción de varianza que aísla el efecto de la política del efecto de la variabilidad aleatoria, facilitando la comparación (Rubinstein &amp; Kroese, 2016, p. 149; Stevens, 2024, p. 87).</p>
</li>
<li>
<p><strong>Calcular estadísticos de desempeño:</strong> Para cada escenario, calcular la media, la varianza y los percentiles de la variable de interés (ej. costo total, tiempo de ciclo).</p>
</li>
<li>
<p><strong>Visualizar la incertidumbre:</strong> La mejor forma de comparar escenarios es visualizar sus distribuciones de probabilidad. Los histogramas superpuestos o, mejor aún, los diagramas de caja y bigotes (<em>box plots</em>) permiten comparar visualmente la mediana, la dispersión y los valores atípicos de cada alternativa de un vistazo (Stevens, 2024, p. 88). Un diagrama de caja muestra la mediana (línea dentro de la caja), el rango intercuartílico (la caja que contiene el 50% central de los datos) y los valores extremos (los “bigotes” y puntos fuera de ellos).</p>
</li>
<li>
<p><strong>Realizar pruebas de hipótesis:</strong> Utilizar pruebas estadísticas formales para determinar si las diferencias observadas entre las medias de los escenarios son estadísticamente significativas (por ejemplo, con un intervalo de confianza para la diferencia de medias) o si podrían deberse simplemente al ruido aleatorio de la simulación (Rubinstein &amp; Kroese, 2016, p. 97).</p>
</li>
<li>
<p><strong>Tomar una decisión:</strong> La decisión final se basa en un análisis holístico de los resultados. No se trata solo de elegir la media más baja, sino de considerar el equilibrio entre el rendimiento esperado y el riesgo (la variabilidad). Un gerente podría preferir una política con un costo esperado ligeramente superior pero con una variabilidad mucho menor (menos riesgo de incurrir en pérdidas catastróficas).</p>
</li>
</ol>
<p><img src="image.png?ejemplos" alt=""> *<strong>Ejemplos de aplicación</strong></p>
<p><strong>Ejemplo 1 (Logística): Simulación de tiempos de entrega</strong><br>
Una empresa de mensajería quiere evaluar el impacto de la compra de una flota de vehículos más rápida en el tiempo de entrega promedio. Se simulan 10,000 días de operación con la flota actual (Escenario A) y con la nueva flota (Escenario B), utilizando los mismos números aleatorios para las llegadas de pedidos. Los resultados muestran que el tiempo de entrega promedio en el Escenario B es 2 horas menor, y un intervalo de confianza del 95% para la diferencia confirma que esta mejora es estadísticamente significativa.</p>
<p><strong>Ejemplo 2 (Inventarios): Simulación de políticas de reposición</strong><br>
Un almacén debe decidir entre dos políticas de reposición de inventario. La simulación Montecarlo de 5,000 semanas de operación arroja los siguientes resultados para el costo total anual (en miles de pesos):</p>

<table>
<thead>
<tr>
<th align="left">Política</th>
<th align="center">Media</th>
<th align="center">Desviación Estándar</th>
<th align="center">Percentil 5</th>
<th align="center">Percentil 95</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left">A (pedidos pequeños y frecuentes)</td>
<td align="center">1,200</td>
<td align="center">150</td>
<td align="center">980</td>
<td align="center">1,450</td>
</tr>
<tr>
<td align="left">B (pedidos grandes y esporádicos)</td>
<td align="center">1,150</td>
<td align="center">280</td>
<td align="center">720</td>
<td align="center">1,680</td>
</tr>
</tbody>
</table><p>Aunque la Política B tiene una media ligeramente menor, su mayor variabilidad implica un riesgo mucho mayor de incurrir en costos muy altos (hasta 1,680). Un gerente adverso al riesgo preferiría la Política A, que ofrece un resultado más predecible.</p>
<p><strong>Ejemplo 3 (Cadena de Suministro): Evaluación de inversión (VAN)</strong><br>
Una empresa evalúa la construcción de un nuevo centro de distribución. Se definen tres escenarios de inversión (baja, media y alta capacidad) y se simula el VAN para cada uno, considerando la incertidumbre en la demanda, los costos de construcción y los precios de los combustibles. Los resultados muestran que el escenario de capacidad media tiene la mayor probabilidad de generar un VAN positivo (85%), mientras que el de alta capacidad, aunque tiene un VAN esperado más alto, también tiene una probabilidad significativa de pérdida (25%). La decisión final dependerá de la tolerancia al riesgo de la empresa.</p>
<p><img src="image.png?cierre_de_tema" alt=""> *<strong>Cierre</strong></p>
<p>Esta octava semana ha completado el ciclo de aplicación del método Montecarlo. Se ha abordado la importancia de la validación de modelos para garantizar la confiabilidad de los resultados. Se ha presentado una guía paso a paso para el desarrollo de una simulación Montecarlo, desde la definición del problema hasta el análisis de resultados. Finalmente, se han introducido las técnicas para la comparación de escenarios, incluyendo el uso de números aleatorios comunes, la visualización con diagramas de caja y la interpretación de resultados para apoyar la toma de decisiones bajo incertidumbre. Con estos conocimientos, se está preparado para la siguiente unidad, donde se abordará la modelación discreta de sistemas, profundizando en la construcción de modelos conceptuales y computacionales para el análisis de sistemas más complejos.</p>
<p><img src="image.png?informaci%C3%B3n_complementaria" alt=""> *<strong>Información complementaria</strong></p>
<p>Se recomienda al estudiantado explorar los siguientes recursos para complementar su aprendizaje:</p>
<ul>
<li><strong>Artículo:</strong> “A Guide to Monte Carlo Simulation in Excel” (disponible en el aula virtual).</li>
<li><strong>Video:</strong> “Monte Carlo Simulation for Decision Making” (serie de videos, enlace en plataforma).</li>
<li><strong>Software:</strong> Practicar la simulación Montecarlo en Excel con la herramienta <code>Simulation</code> (complemento gratuito) o en Python con las librerías <code>numpy</code> y <code>matplotlib</code>.</li>
<li><strong>Caso práctico:</strong> Revisar ejemplos de análisis de riesgo en proyectos de inversión utilizando simulación Montecarlo.</li>
</ul>
<p><img src="image.png?referencias" alt=""> *<strong>Referencias</strong></p>
<p>Rubinstein, R. Y., &amp; Kroese, D. P. (2016). <em>Simulation and the Monte Carlo method</em> (3rd ed.). John Wiley &amp; Sons.</p>
<p>Shonkwiler, R. W., &amp; Mendivil, F. (2024). <em>Explorations in Monte Carlo methods</em> (2nd ed.). Springer.</p>
<p>Stevens, A. (2024). <em>Monte-Carlo simulation: An introduction for engineers and scientists</em>. CRC Press.</p>
</div>
</body>

</html>
