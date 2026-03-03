<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CONTENIDO SEMANA 2</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><hr>
<h1 id="teoría-de-sistemas-y-simulación---semana-2">TEORÍA DE SISTEMAS Y SIMULACIÓN - SEMANA 2</h1>
<h2 id="unidad-1-teoría-de-decisiones-continuación">UNIDAD 1: TEORÍA DE DECISIONES (Continuación)</h2>
<p>En la semana anterior se establecieron los fundamentos conceptuales de la teoría de decisiones, explorando los elementos de un problema de decisión, los tipos de entornos y los criterios para elegir la mejor alternativa. En esta segunda semana, se profundiza en las herramientas que permiten estructurar y analizar problemas de decisión más complejos. La matriz de pagos se consolida como la base para representar y aplicar los criterios ya estudiados. A continuación, se introduce el árbol de decisión, una poderosa herramienta gráfica que permite modelar problemas con secuencias de decisiones a lo largo del tiempo y la incorporación de nueva información para reducir la incertidumbre.</p>
<p><img src="image.png?conceptos_clave" alt=""> <em><strong>Conceptos clave</strong></em></p>
<ul>
<li><strong>Matriz de pagos:</strong> Representación tabular que cruza las alternativas del decisor con los posibles estados de la naturaleza, mostrando el resultado de cada combinación.</li>
<li><strong>Árbol de decisión:</strong> Representación gráfica que mapea todas las posibles secuencias de decisiones, eventos inciertos y resultados en un problema.</li>
<li><strong>Nodo de decisión (□):</strong> Punto en el árbol donde el decisor debe elegir entre dos o más cursos de acción.</li>
<li><strong>Nodo de probabilidad (○):</strong> Punto donde ocurre un evento incierto fuera del control del decisor, con ramas que tienen probabilidades asociadas.</li>
<li><strong>Nodo terminal (▼):</strong> Punto que representa el final de una secuencia y donde se registra el pago final.</li>
<li><strong>Inducción hacia atrás (folding back):</strong> Método de evaluación de árboles de decisión que consiste en calcular de derecha a izquierda los valores esperados y las decisiones óptimas.</li>
</ul>
<p><img src="image.png?contenido" alt=""> <em><strong>Desarrollo del contenido</strong></em></p>
<h3 id="matriz-de-salidas-o-tabla-de-pagos">1.4 Matriz de salidas o tabla de pagos</h3>
<h4 id="definición-y-concepto">Definición y concepto</h4>
<p>La <strong>matriz de pagos</strong> (también conocida como matriz de resultados o tabla de pagos) es una herramienta fundamental para representar problemas de decisión en los que un decisor debe elegir entre varias alternativas bajo incertidumbre sobre el futuro. Como señalan Bautista &amp; López (2015, p. 5), la matriz de pagos es la base para aplicar los diferentes criterios de decisión y constituye un elemento central de la teoría de decisión.</p>
<p>Una matriz de pagos es una representación tabular que cruza las <strong>alternativas</strong> del decisor con los posibles <strong>estados de la naturaleza</strong>. Cada celda de la matriz contiene el <strong>pago</strong> (resultado cuantitativo) que se obtendría si se eligiera una alternativa específica y ocurriera un estado de la naturaleza particular.</p>
<h4 id="estructura-de-la-matriz-de-pagos">Estructura de la matriz de pagos</h4>
<p>La estructura general de una matriz de pagos es la siguiente (Bautista &amp; López, 2015, p. 5):</p>
<p><strong>Tabla 1</strong><br>
<em>Estructura general de una matriz de pagos</em></p>

<table>
<thead>
<tr>
<th align="left"></th>
<th align="center"><strong>Estado s₁</strong></th>
<th align="center"><strong>Estado s₂</strong></th>
<th align="center"><strong>…</strong></th>
<th align="center"><strong>Estado sₘ</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Acción a₁</strong></td>
<td align="center">u₁₁</td>
<td align="center">u₁₂</td>
<td align="center">…</td>
<td align="center">u₁ₘ</td>
</tr>
<tr>
<td align="left"><strong>Acción a₂</strong></td>
<td align="center">u₂₁</td>
<td align="center">u₂₂</td>
<td align="center">…</td>
<td align="center">u₂ₘ</td>
</tr>
<tr>
<td align="left"><strong>…</strong></td>
<td align="center">…</td>
<td align="center">…</td>
<td align="center">…</td>
<td align="center">…</td>
</tr>
<tr>
<td align="left"><strong>Acción aₙ</strong></td>
<td align="center">uₙ₁</td>
<td align="center">uₙ₂</td>
<td align="center">…</td>
<td align="center">uₙₘ</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Bautista &amp; López (2015).</p>
<p>Donde:</p>
<ul>
<li><strong>aᵢ</strong> (i = 1, 2, …, n): Acciones o alternativas disponibles para el decisor</li>
<li><strong>sⱼ</strong> (j = 1, 2, …, m): Estados de la naturaleza (escenarios futuros)</li>
<li><strong>uᵢⱼ</strong>: Utilidad o resultado obtenido al elegir la acción aᵢ cuando ocurre el estado sⱼ</li>
</ul>
<h4 id="elementos-de-la-matriz-de-pagos">Elementos de la matriz de pagos</h4>
<p><strong>Alternativas (acciones):</strong> Son los cursos de acción que el decisor puede controlar. Deben ser mutuamente excluyentes (elegir una implica no elegir las otras) y colectivamente exhaustivas (cubren todas las opciones relevantes). En el contexto de la dirección estratégica, las estrategias son los medios por los cuales se logran los objetivos a largo plazo (David, 2013, p. 11).</p>
<p><strong>Estados de la naturaleza:</strong> Son las situaciones o escenarios futuros que están fuera del control del decisor. Se refieren a tendencias y sucesos económicos, sociales, culturales, demográficos, ambientales, políticos, legales, tecnológicos y competitivos que pudieran beneficiar o dañar en forma significativa a una empresa en el futuro (David, 2013, p. 10).</p>
<p><strong>Pagos (utilidades):</strong> Es la evaluación de las consecuencias al elegir una determinada acción frente a un determinado estado. Pueden expresarse como ganancias, pérdidas, beneficios, costos, etc. (Bautista &amp; López, 2015, p. 4).</p>
<h4 id="construcción-de-una-matriz-de-pagos">Construcción de una matriz de pagos</h4>
<p>Para construir una matriz de pagos, se deben seguir los siguientes pasos:</p>
<ol>
<li><strong>Identificar las alternativas:</strong> Listar todos los cursos de acción posibles bajo control del decisor.</li>
<li><strong>Identificar los estados de la naturaleza:</strong> Listar todos los escenarios futuros relevantes fuera del control del decisor.</li>
<li><strong>Determinar los pagos:</strong> Calcular el resultado (beneficio, costo, etc.) para cada combinación acción-estado.</li>
<li><strong>Organizar en forma tabular:</strong> Colocar las alternativas en filas, los estados en columnas y los pagos en las celdas correspondientes.</li>
</ol>
<h4 id="ejemplos-de-matrices-de-pagos-para-ingeniería-industrial-y-logística">Ejemplos de matrices de pagos para Ingeniería Industrial y Logística</h4>
<p><strong>Ejemplo 1 (Industria): Decisión de capacidad de producción</strong></p>
<p>Una planta manufacturera debe decidir su nivel de capacidad para el próximo trimestre. La demanda puede ser baja, media o alta. Los beneficios (en millones de pesos) son:</p>
<p><strong>Tabla 2</strong><br>
<em>Matriz de pagos para decisión de capacidad</em></p>

<table>
<thead>
<tr>
<th align="left">Acción</th>
<th align="center">Demanda Baja</th>
<th align="center">Demanda Media</th>
<th align="center">Demanda Alta</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Capacidad Baja (1000 u/día)</strong></td>
<td align="center">50</td>
<td align="center">60</td>
<td align="center">70</td>
</tr>
<tr>
<td align="left"><strong>Capacidad Media (1500 u/día)</strong></td>
<td align="center">40</td>
<td align="center">80</td>
<td align="center">100</td>
</tr>
<tr>
<td align="left"><strong>Capacidad Alta (2000 u/día)</strong></td>
<td align="center">10</td>
<td align="center">70</td>
<td align="center">130</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Elaboración propia.</p>
<p><strong>Interpretación:</strong> Si se elige Capacidad Media y la demanda resulta ser Alta, el beneficio obtenido será de 100 millones de pesos.</p>
<p><strong>Ejemplo 2 (Logística): Decisión de modo de transporte</strong></p>
<p>Una empresa exportadora debe elegir el modo de transporte para un envío urgente. El costo total depende del modo elegido y del tiempo real de tránsito (incierto). Los costos (en miles de dólares) son:</p>
<p><strong>Tabla 3</strong><br>
<em>Matriz de pagos para decisión de modo de transporte</em></p>

<table>
<thead>
<tr>
<th align="left">Acción</th>
<th align="center">Tiempo Normal</th>
<th align="center">Tiempo con Retraso</th>
<th align="center">Tiempo con Demora Crítica</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Transporte Marítimo</strong></td>
<td align="center">15</td>
<td align="center">25</td>
<td align="center">40</td>
</tr>
<tr>
<td align="left"><strong>Transporte Aéreo</strong></td>
<td align="center">30</td>
<td align="center">35</td>
<td align="center">45</td>
</tr>
<tr>
<td align="left"><strong>Transporte Terrestre (urgente)</strong></td>
<td align="center">20</td>
<td align="center">30</td>
<td align="center">55</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Elaboración propia.</p>
<p><strong>Interpretación:</strong> Si se elige Transporte Aéreo y ocurre un retraso, el costo será de 35 mil dólares.</p>
<p><strong>Ejemplo 3 (Inventarios): Decisión de nivel de inventario de seguridad</strong></p>
<p>Un centro de distribución debe decidir su nivel de inventario de seguridad para la temporada navideña. La demanda puede ser baja, media o alta. Los costos totales (incluyendo faltantes y obsolescencia) son:</p>
<p><strong>Tabla 4</strong><br>
<em>Matriz de pagos para decisión de inventario de seguridad</em></p>

<table>
<thead>
<tr>
<th align="left">Acción</th>
<th align="center">Demanda Baja</th>
<th align="center">Demanda Media</th>
<th align="center">Demanda Alta</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Inventario Bajo (500 u)</strong></td>
<td align="center">20</td>
<td align="center">40</td>
<td align="center">80</td>
</tr>
<tr>
<td align="left"><strong>Inventario Medio (800 u)</strong></td>
<td align="center">30</td>
<td align="center">30</td>
<td align="center">50</td>
</tr>
<tr>
<td align="left"><strong>Inventario Alto (1200 u)</strong></td>
<td align="center">50</td>
<td align="center">40</td>
<td align="center">30</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Elaboración propia.</p>
<p><strong>Interpretación:</strong> Si se elige Inventario Alto y la demanda resulta ser Baja, el costo será de 50 mil pesos.</p>
<h4 id="tipos-de-matrices-según-el-entorno-de-decisión">Tipos de matrices según el entorno de decisión</h4>
<p>Dependiendo del tipo de universo de decisión (Bautista &amp; López, 2015, p. 3), la matriz de pagos se utiliza de diferentes maneras:</p>
<p><strong>Tabla 5</strong><br>
<em>Uso de la matriz de pagos según el entorno de decisión</em></p>

<table>
<thead>
<tr>
<th align="left">Tipo de universo</th>
<th align="left">Uso de la matriz de pagos</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Determinista</strong></td>
<td align="left">Se conoce con certeza el estado que ocurrirá; la matriz sirve para identificar la mejor acción para ese estado específico.</td>
</tr>
<tr>
<td align="left"><strong>Aleatorio (Riesgo)</strong></td>
<td align="left">Se conocen las probabilidades de cada estado; la matriz es la base para calcular el valor esperado de cada acción.</td>
</tr>
<tr>
<td align="left"><strong>Incierto</strong></td>
<td align="left">No se conocen probabilidades; la matriz es la base para aplicar criterios como Maximax, Maximin, Hurwicz, Laplace y Savage.</td>
</tr>
<tr>
<td align="left"><strong>Hostil</strong></td>
<td align="left">La matriz puede extenderse a teoría de juegos, considerando que los estados son acciones de otros decisores.</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Elaboración propia con base en Bautista &amp; López (2015).</p>
<h3 id="árboles-de-decisión">1.5 Árboles de decisión</h3>
<h4 id="definición-y-concepto-1">Definición y concepto</h4>
<p>Un <strong>árbol de decisión</strong> es una representación gráfica que mapea todas las posibles secuencias de decisiones, eventos inciertos y resultados en un problema (Bautista &amp; López, 2015, p. 25). Mientras que la matriz de pagos es ideal para problemas de una sola decisión, muchos problemas del mundo real involucran una <strong>secuencia de decisiones</strong> a lo largo del tiempo, donde las decisiones tempranas afectan las opciones disponibles en el futuro y donde se puede obtener nueva información que reduce la incertidumbre. Para estos casos, el árbol de decisión es la herramienta más adecuada.</p>
<h4 id="elementos-de-un-árbol-de-decisión">Elementos de un árbol de decisión</h4>
<p>Los árboles de decisión constan de tres tipos de elementos (Bautista &amp; López, 2015, p. 25):</p>
<p><strong>Tabla 6</strong><br>
<em>Elementos de un árbol de decisión</em></p>

<table>
<thead>
<tr>
<th align="left">Elemento</th>
<th align="center">Símbolo</th>
<th align="left">Descripción</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Nodo de decisión</strong></td>
<td align="center">□</td>
<td align="left">Representa puntos en el tiempo donde el decisor debe elegir entre dos o más cursos de acción. De estos nodos parten ramas que representan las alternativas.</td>
</tr>
<tr>
<td align="left"><strong>Nodo de probabilidad</strong></td>
<td align="center">○</td>
<td align="left">Representa puntos donde ocurre un evento incierto (un estado de la naturaleza) fuera del control del decisor. De estos nodos parten ramas que representan los posibles resultados del evento, cada una con su probabilidad asociada.</td>
</tr>
<tr>
<td align="left"><strong>Nodo terminal</strong></td>
<td align="center">▼</td>
<td align="left">Representa el final de una secuencia particular de decisiones y eventos. En estos nodos se registra el pago o utilidad final de esa trayectoria.</td>
</tr>
<tr>
<td align="left"><strong>Ramas</strong></td>
<td align="center">—</td>
<td align="left">Líneas que conectan los nodos, representando las alternativas o los resultados de eventos inciertos.</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Bautista &amp; López (2015).</p>
<h4 id="construcción-y-evaluación-de-árboles-de-decisión">Construcción y evaluación de árboles de decisión</h4>
<p>El proceso de construir y evaluar un árbol de decisión sigue un enfoque sistemático conocido como <strong>“folding back”</strong> o inducción hacia atrás (Bautista &amp; López, 2015, pp. 25-26):</p>
<p><strong>Paso 1: Estructuración del problema</strong><br>
Identificar la secuencia lógica de decisiones y eventos inciertos, dibujando el árbol de izquierda a derecha, comenzando con la primera decisión.</p>
<p><strong>Paso 2: Asignación de probabilidades</strong><br>
Asignar probabilidades a cada rama que emana de un nodo de probabilidad. Estas probabilidades deben reflejar el conocimiento actual del decisor sobre la ocurrencia de cada evento.</p>
<p><strong>Paso 3: Asignación de pagos</strong><br>
Asignar un valor (utilidad, costo, beneficio) a cada nodo terminal, reflejando el resultado final de esa trayectoria.</p>
<p><strong>Paso 4: Evaluación (folding back)</strong><br>
El árbol se evalúa de derecha a izquierda:</p>
<ul>
<li>En un <strong>nodo de probabilidad</strong> (○), se calcula el <strong>valor esperado</strong> de las ramas que emanan de él: <code>VE = Σ (pⱼ × resultadoⱼ)</code></li>
<li>En un <strong>nodo de decisión</strong> (□), se selecciona la rama (alternativa) que proporciona el mayor valor esperado (o el menor costo esperado), y ese valor se asigna al nodo.</li>
</ul>
<p><strong>Paso 5: Selección de la estrategia óptima</strong><br>
La secuencia de decisiones que conduce al mayor valor esperado en el nodo de decisión inicial constituye la estrategia óptima.</p>
<h4 id="ejemplo-de-árbol-de-decisión-para-ingeniería-industrial">Ejemplo de árbol de decisión para Ingeniería Industrial</h4>
<p><strong>Ejemplo 4: Decisión de ampliación con estudio de mercado</strong></p>
<p>Una empresa manufacturera debe decidir si ampliar su planta ahora o esperar un año. Si amplía ahora, puede obtener beneficios de 100, 80 o 60 millones dependiendo de si la demanda es alta, media o baja (con probabilidades 0.3, 0.4 y 0.3 respectivamente).</p>
<p>Si espera un año, puede realizar un estudio de mercado (costo de 5 millones) que le dará información sobre la demanda futura. El estudio tiene una confiabilidad del 80% (probabilidad de que el estudio acierte el estado real).</p>
<p><strong>Figura 1</strong><br>
<em>Árbol de decisión para el problema de ampliación</em></p>
<pre><code>                      ┌── Demanda Alta (0.3) ── 100
                      │
              ┌──○──┼── Demanda Media (0.4) ── 80
              │      │
              │      └── Demanda Baja (0.3) ── 60
              │
      ┌──□──┤
      │      │      ┌── Demanda Alta ── 100 - 5 = 95
      │      │      │
      │      └──□──┼── Demanda Media ── 80 - 5 = 75
      │             │
      │             └── Demanda Baja ── 60 - 5 = 55
      │
──□──┤
      │
      │             ┌── Estudio predice Alta ──□── (decisiones condicionales)
      │             │
      └──□──┼── Estudio predice Media ──□──
                    │
                    └── Estudio predice Baja ──□──
</code></pre>
<p><em>Fuente:</em> Elaboración propia.</p>
<p><strong>Evaluación (folding back):</strong></p>
<p><strong>Paso 1:</strong> Calcular el valor esperado de ampliar ahora</p>
<pre><code>VE(ampliar ahora) = 0.3×100 + 0.4×80 + 0.3×60 = 30 + 32 + 18 = 80
</code></pre>
<p><strong>Paso 2:</strong> Para la opción de esperar y hacer estudio, necesitamos:</p>
<ul>
<li>Probabilidades a priori: P(Alta)=0.3, P(Media)=0.4, P(Baja)=0.3</li>
<li>Confiabilidad del estudio: 80% de acierto</li>
</ul>
<p>Las probabilidades condicionales P(estudio predice X | estado real Y) son:</p>
<ul>
<li>Si el estudio es confiable al 80%, entonces P(predice Alta | Alta) = 0.8</li>
<li>El 20% restante se distribuye entre los otros dos estados (supongamos 10% cada uno)</li>
</ul>
<p><strong>Paso 3:</strong> Calcular probabilidades conjuntas y marginales (Teorema de Bayes)</p>
<p><strong>Paso 4:</strong> Para cada resultado del estudio, calcular el valor esperado de las decisiones condicionales</p>
<p><strong>Paso 5:</strong> Comparar VE(ampliar ahora) = 80 vs VE(esperar con estudio) = ?</p>
<p><em>Nota: Este ejemplo se desarrollará completamente en la Actividad 1.</em></p>
<h4 id="aplicación-a-problemas-logísticos">Aplicación a problemas logísticos</h4>
<p><strong>Ejemplo 5: Decisión de transporte con información de tracking</strong></p>
<p>Una empresa debe enviar un cargamento urgente. Puede elegir entre transporte marítimo (más barato pero lento) o aéreo (más rápido pero costoso). Si elige marítimo y el barco llega a tiempo, el costo es 15; si llega con retraso, el costo es 25; si llega con demora crítica, el costo es 40 (por penalizaciones). Si elige aéreo, los costos son 30, 35 y 45 respectivamente.</p>
<p>La empresa puede contratar un servicio de tracking satelital (costo 3) que le dará información más precisa sobre el tiempo de tránsito real.</p>
<p><strong>Ventajas del árbol de decisión:</strong></p>
<ol>
<li><strong>Visualiza la secuencia:</strong> Muestra claramente el orden de las decisiones y eventos.</li>
<li><strong>Incorpora nueva información:</strong> Permite modelar cómo la información (como el tracking) modifica las probabilidades a través del Teorema de Bayes.</li>
<li><strong>Evalúa estrategias condicionales:</strong> Permite definir “si ocurre X, entonces hacer Y”.</li>
<li><strong>Calcula el valor de la información:</strong> Permite determinar si vale la pena pagar por información adicional.</li>
</ol>
<h4 id="relación-entre-matriz-de-pagos-y-árbol-de-decisión">Relación entre matriz de pagos y árbol de decisión</h4>
<p><strong>Tabla 7</strong><br>
<em>Comparación entre matriz de pagos y árbol de decisión</em></p>

<table>
<thead>
<tr>
<th align="left">Herramienta</th>
<th align="left">Cuándo usarla</th>
<th align="left">Ventajas</th>
<th align="left">Limitaciones</th>
</tr>
</thead>
<tbody>
<tr>
<td align="left"><strong>Matriz de pagos</strong></td>
<td align="left">Problemas de una sola decisión, con múltiples estados de la naturaleza</td>
<td align="left">Simple, fácil de construir, base para criterios de decisión</td>
<td align="left">No maneja secuencias de decisiones, no incorpora información nueva fácilmente</td>
</tr>
<tr>
<td align="left"><strong>Árbol de decisión</strong></td>
<td align="left">Problemas con secuencias de decisiones, posibilidad de obtener información adicional</td>
<td align="left">Visualiza la secuencia, maneja decisiones condicionales, incorpora probabilidades bayesianas</td>
<td align="left">Más complejo de construir, requiere más información</td>
</tr>
</tbody>
</table><p><em>Fuente:</em> Elaboración propia.</p>
<p>Ambas herramientas son complementarias: la matriz de pagos es la base para los nodos terminales del árbol, y los criterios de decisión vistos en la Semana 1 se aplican en los nodos de probabilidad y decisión del árbol.</p>
<p><img src="image.png?cierre_de_tema" alt=""> <em><strong>Cierre</strong></em></p>
<p>En esta segunda semana se han consolidado dos herramientas fundamentales para el análisis de problemas de decisión: la matriz de pagos y los árboles de decisión. La matriz de pagos, como representación tabular, permite estructurar y aplicar los criterios de decisión estudiados en la semana anterior, siendo la base para problemas de una sola decisión. Por su parte, los árboles de decisión extienden esta capacidad al permitir modelar problemas más complejos que involucran secuencias de decisiones a lo largo del tiempo y la incorporación de nueva información, como estudios de mercado o sistemas de tracking. Estos conocimientos preparan el terreno para adentrarse en el análisis de sistemas más complejos, como las líneas de espera, que se abordarán en las siguientes semanas.</p>
<p><img src="image.png?informaci%C3%B3n_complementaria" alt=""> <em><strong>Información complementaria</strong></em></p>
<p>Se recomienda al estudiantado explorar los siguientes recursos para complementar su aprendizaje:</p>
<ul>
<li><strong>Artículo:</strong> “Decision Trees: A Primer for Decision-Making Under Uncertainty” (disponible en el aula virtual).</li>
<li><strong>Video:</strong> “Árboles de Decisión - Teoría y Ejemplos Prácticos” (enlace en plataforma).</li>
<li><strong>Software:</strong> Explorar herramientas gratuitas en línea para dibujar árboles de decisión (por ejemplo, <a href="http://draw.io">draw.io</a>, Lucidchart).</li>
<li><strong>Caso práctico:</strong> Revisar ejemplos de árboles de decisión en la industria farmacéutica para decisiones de inversión en I+D.</li>
</ul>
<p><img src="image.png?referencias" alt=""> <em><strong>Referencias</strong></em></p>
<p>Bautista, J., &amp; López, G. (2015). <em>Fundamentos de Teoría de la Decisión</em>. Modelos y Herramientas de Decisión – Máster Universitario de Ingeniería de Organización. Universitat Politècnica de Catalunya – BarcelonaTech.</p>
<p>David, F. R. (2013). <em>Conceptos de administración estratégica</em> (14a ed.). Pearson Educación.</p>
</div>
</body>

</html>
