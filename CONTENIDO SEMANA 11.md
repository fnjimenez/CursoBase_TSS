<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CONTENIDO SEMANA 11</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__html"><hr>
<h1 id="tteoría-de-sistemas-y-simulación---semana-11">TTEORÍA DE SISTEMAS Y SIMULACIÓN - SEMANA 11</h1>
<h2 id="unidad-5-modelación-discreta-de-sistemas-continuación">UNIDAD 5: MODELACIÓN DISCRETA DE SISTEMAS (Continuación)</h2>
<p>En la semana anterior se abordaron las técnicas para el análisis de resultados de simulaciones y cómo estos pueden utilizarse para el mejoramiento de procesos y la toma de decisiones. El caso de estudio de la planta de Cambay demostró el valor práctico de la simulación para diagnosticar cuellos de botella y evaluar alternativas de mejora. Esta semana se profundiza en el proceso de construcción de modelos computacionales, explorando los elementos y comandos específicos que ofrecen los paquetes de simulación modernos. Utilizando AnyLogic como plataforma de referencia, se describirán los componentes básicos y avanzados para modelar sistemas de eventos discretos, así como los comandos y fragmentos de código que permiten personalizar el comportamiento del modelo más allá de los bloques predefinidos, completando así el ciclo de modelación discreta de sistemas.</p>
<p><img src="image.png?conceptos_clave" alt=""> *<strong>Conceptos clave</strong></p>
<ul>
<li><strong>Estructura estática:</strong> Representación de los elementos fijos del sistema en el modelo, como los espacios físicos y los recursos.</li>
<li><strong>Estructura dinámica:</strong> Implementación del flujo de entidades y la lógica de eventos en el modelo computacional.</li>
<li><strong>ResourcePool:</strong> Conjunto de recursos (humanos o equipos) que pueden ser asignados dinámicamente a las entidades durante la simulación.</li>
<li><strong>Bloque <code>Seize</code>:</strong> Bloque que modela la toma de un recurso por parte de una entidad, generando una espera si el recurso no está disponible.</li>
<li><strong>Bloque <code>Delay</code>:</strong> Bloque que representa una actividad con una duración determinada (tiempo de proceso).</li>
<li><strong>Bloque <code>Release</code>:</strong> Bloque que libera un recurso previamente tomado, dejándolo disponible para otras entidades.</li>
<li><strong>Bloque <code>SelectOutput</code>:</strong> Bloque que introduce lógica de decisión en el flujo, dirigiendo entidades por diferentes caminos según condiciones.</li>
<li><strong>Bloque <code>Hold</code>:</strong> Bloque que retiene entidades hasta que se cumpla una condición específica, modelando dependencias entre procesos.</li>
<li><strong>Comandos Java:</strong> Fragmentos de código que permiten extender la funcionalidad de los bloques predefinidos y personalizar la lógica del modelo.</li>
</ul>
<p><img src="image.png?contenido" alt=""> *<strong>Desarrollo del contenido</strong></p>
<h3 id="construcción-de-modelos-conceptual-y-computacional-aplicado-con-software">5.6 Construcción de Modelos Conceptual y Computacional (aplicado con software)</h3>
<p>Una vez que se han comprendido los fundamentos teóricos de los sistemas de eventos discretos y las estrategias de simulación, el siguiente paso es la materialización de estos conceptos en un modelo computacional funcional. Este proceso, conocido como <em>implementación</em>, consiste en traducir el modelo conceptual (la abstracción lógica del sistema real) a un programa ejecutable dentro de un software de simulación específico (Condon et al., 2025, p. 46).</p>
<h4 id="del-modelo-conceptual-al-modelo-en-anylogic">Del modelo conceptual al modelo en AnyLogic</h4>
<p>El caso de estudio de la planta de polvos de Industrias Alimentarias Cambay S.A. (Condon et al., 2025) proporciona una hoja de ruta ejemplar de este proceso. El punto de partida es el modelo conceptual, representado en este caso por el diagrama de flujo y ciclo de actividades y el diagrama de límites del sistema. Este modelo conceptual identifica las entidades clave (órdenes de producción), los recursos (personal, balanzas, mezcladoras, envasadoras) y las reglas de operación (flujo de materiales, asignación de personal, dependencias entre órdenes de semielaborado y producto terminado).</p>
<p>La construcción del modelo computacional en AnyLogic se realiza en dos etapas fundamentales: la definición de la <strong>estructura estática</strong> y la programación de la <strong>estructura dinámica</strong>.</p>
<h4 id="definición-de-la-estructura-estática-la-fábrica-de-iconos">Definición de la estructura estática: la fábrica de iconos</h4>
<p>La estructura estática define el “escenario” donde ocurrirá la simulación. En AnyLogic, esto se logra mediante la creación de un modelo 2D (o 3D) que representa los espacios físicos y los recursos fijos del sistema. Para el caso de Cambay, se utilizó el archivo CAD del layout de la planta para delimitar las áreas de trabajo (Condon et al., 2025, p. 49). Aunque las distancias no son relevantes para los tiempos de proceso, el layout 2D simplificado es una herramienta visual poderosa para:</p>
<ul>
<li><strong>Verificar el flujo de entidades:</strong> Observar si las órdenes se mueven correctamente entre las estaciones (balanzas, mezcladoras, calidad, envasado, etc.).</li>
<li><strong>Identificar cuellos de botella visualmente:</strong> Acumulaciones de entidades delante de una máquina son una señal inmediata de un posible cuello de botella.</li>
<li><strong>Comunicar el modelo:</strong> Un modelo visual es mucho más fácil de entender y validar por parte de los stakeholders (como el jefe de planta) que una serie de ecuaciones o código (Condon et al., 2025, p. 64).</li>
</ul>
<p>En esta representación estática, los <strong>recursos</strong> se definen mediante <code>ResourcePools</code>. En el modelo de Cambay, se diferencian dos tipos de recursos (Condon et al., 2025, p. 50):</p>
<ul>
<li><strong>Recursos estáticos:</strong> Las máquinas y equipos. Por ejemplo, <code>Pool_Mezcladora_100</code>, <code>Pool_Envasadora_05</code>. Su capacidad es fija y representan el número de máquinas idénticas disponibles.</li>
<li><strong>Recursos móviles:</strong> El personal, categorizado por su nivel de habilidad (<code>Pool_Personal_N1</code>, <code>Pool_Personal_N2</code>, <code>Pool_Personal_N3</code>). Estos recursos se “mueven” con la entidad (la orden) a lo largo del proceso, reflejando la realidad de que un operario transporta materiales o acompaña a una orden.</li>
</ul>
<h3 id="elementos-básicos-y-avanzados-del-paquete-de-simulación">5.7 Elementos Básicos y Avanzados del Paquete de Simulación</h3>
<p>AnyLogic, como entorno de simulación, ofrece una gama de elementos que permiten al modelador elegir el nivel de detalle y complejidad adecuado para su estudio.</p>
<h4 id="programación-de-la-estructura-dinámica-el-flujo-de-la-vida">Programación de la estructura dinámica: el flujo de la vida</h4>
<p>La estructura dinámica es el “alma” del modelo. En AnyLogic, para sistemas de eventos discretos, esto se implementa arrastrando y conectando bloques de la librería <code>Process Modeling Library</code> (Condon et al., 2025, p. 53). La secuencia típica de bloques para modelar una actividad en una estación de trabajo sigue el patrón: <strong><code>Seize</code> → <code>Move To</code> → <code>Delay</code> → <code>Release</code></strong> (Condon et al., 2025, p. 53).</p>
<ul>
<li>
<p><strong><code>Source</code> (Fuente):</strong> El punto de partida. Genera las “entidades” (los agentes) que fluirán por el modelo. En Cambay, el <code>source</code> genera las Órdenes de Producción (OP) cargadas desde una base de datos, diferenciando si son de Semielaborado (SE) o Producto Terminado (PT) (Condon et al., 2025, p. 51).</p>
</li>
<li>
<p><strong><code>Seize</code> (Tomar):</strong> Es el bloque que modela la competencia por un recurso escaso. Cuando una orden llega a este bloque, solicita una unidad de un <code>ResourcePool</code> específico (por ejemplo, un operario de categoría 2 y una mezcladora de 500 kg). Si los recursos están disponibles, los “captura” y la orden avanza. Si no, la orden espera en una cola interna del bloque (Condon et al., 2025, p. 53). En el modelo de Cambay, este bloque es crítico para modelar la asignación de personal con diferentes categorías, donde se pueden usar conjuntos de recursos alternativos. Una característica avanzada es la definición de <strong>prioridades</strong>: las órdenes que ya tienen <strong>todos</strong> sus recursos disponibles tienen preferencia sobre aquellas que solo tienen algunos, modelando la flexibilidad operativa de la planta (Condon et al., 2025, p. 55).</p>
</li>
<li>
<p><strong><code>Move To</code> (Mover a):</strong> Simula el traslado físico de la entidad a la ubicación donde se realizará la actividad. Una opción clave es <code>Attach Seized Resources</code>, que permite que los recursos capturados (como el personal) se desplacen con la entidad, reflejando fielmente la realidad operativa (Condon et al., 2025, p. 53).</p>
</li>
<li>
<p><strong><code>Delay</code> (Demora):</strong> Es el bloque que representa la actividad en sí misma. Aquí es donde se programa el <strong>tiempo de procesamiento</strong>. Este tiempo puede ser constante, o puede ser una función de los atributos de la entidad. En Cambay, los tiempos de procesamiento se calculan en función de la cantidad a producir (<code>qsku</code>) y la máquina utilizada. Por ejemplo, el tiempo en una mezcladora se calcula como el número de mezclas necesarias (redondeado al entero superior) multiplicado por el tiempo estándar de la máquina (Condon et al., 2025, p. 56).</p>
</li>
<li>
<p><strong><code>Release</code> (Liberar):</strong> Una vez que el <code>Delay</code> termina, la actividad ha concluido. El bloque <code>Release</code> devuelve los recursos capturados al <code>ResourcePool</code>, dejándolos disponibles para que otras entidades los tomen (Condon et al., 2025, p. 53).</p>
</li>
<li>
<p><strong><code>Sink</code> (Sumidero):</strong> El punto final. Cuando una orden ha completado todo su procesamiento, llega a este bloque y es “destruida”. El modelo de Cambay utiliza un mecanismo para detener la simulación: cada vez que una orden llega a un <code>Sink</code>, incrementa un contador. Cuando el contador alcanza el número total de órdenes a procesar, la simulación termina automáticamente (Condon et al., 2025, p. 58).</p>
</li>
</ul>
<p>Esta estructura se repite a lo largo de todo el flujo de producción, creando una red interconectada de actividades que imita fielmente el proceso real.</p>
<h4 id="elementos-avanzados-para-lógica-de-decisión">Elementos avanzados para lógica de decisión</h4>
<ul>
<li>
<p><strong><code>SelectOutput</code> (Salida condicional):</strong> Este bloque introduce la lógica de decisión en el modelo. En Cambay, se utiliza para dirigir una orden a la máquina correcta según sus atributos. Por ejemplo, en la estación de mezclado, un bloque <code>SelectOutput</code> evalúa la cantidad de la orden (<code>agent.qsku</code>) y la envía a la cola de la mezcladora de 100 kg, 200 kg, 500 kg o 2500 kg. Lo mismo ocurre para dirigir los productos a la envasadora correcta según su gramaje (Condon et al., 2025, p. 51).</p>
</li>
<li>
<p><strong><code>Hold</code> (Retener):</strong> Este bloque es fundamental para modelar dependencias entre procesos. En Cambay, las órdenes de Producto Terminado (PT) no pueden comenzar hasta que su correspondiente orden de Semielaborado (SE) haya finalizado. Cuando se genera una orden PT, entra en una cola conectada a un bloque <code>Hold</code>. El bloque <code>Hold</code> actúa como una compuerta: impide el paso de las órdenes PT hasta que se cumpla una condición (Condon et al., 2025, p. 51). La liberación se programa mediante código Java (ver Sección 5.8).</p>
</li>
</ul>
<h3 id="comandos-utilizados-en-el-paquete-de-simulación">5.8 Comandos Utilizados en el Paquete de Simulación</h3>
<p>La verdadera potencia de AnyLogic radica en su capacidad para ser extendido mediante el lenguaje de programación Java. Los “comandos” no son instrucciones aisladas, sino fragmentos de código que se insertan en las acciones de los bloques para personalizar su comportamiento (Condon et al., 2025, p. 52).</p>
<h4 id="java-como-el-lenguaje-de-control">Java como el lenguaje de control</h4>
<p>El uso de Java permite ir más allá de la configuración estándar de los bloques y programar la lógica específica del sistema. Los dos ejemplos más claros en el modelo de Cambay son:</p>
<ul>
<li>
<p><strong>Comando para liberar órdenes de producción (<code>Hold</code>):</strong> Cuando una orden de Semielaborado (SE) finaliza en el bloque <code>sink</code>, se ejecuta un código que recorre la lista completa de todas las órdenes pendientes (almacenadas en un <code>array</code>). Este código busca las órdenes de Producto Terminado (PT) cuyo <code>predecesor</code> coincide con el <code>id_op</code> de la orden SE que acaba de terminar. Cuando encuentra una coincidencia, cambia su parámetro <code>liberado</code> a <code>true</code> (Condon et al., 2025, p. 52).</p>
<pre class=" language-java"><code class="prism  language-java"><span class="token comment">// Actualizar los valores de liberado en la lista</span>
<span class="token keyword">for</span> <span class="token punctuation">(</span>OP_SE miAgente <span class="token operator">:</span> var_listaOP<span class="token punctuation">)</span> <span class="token punctuation">{</span>
  <span class="token keyword">if</span> <span class="token punctuation">(</span>miAgente<span class="token punctuation">.</span>predecesor <span class="token operator">!=</span> null <span class="token operator">&amp;&amp;</span> miAgente<span class="token punctuation">.</span>predecesor<span class="token punctuation">.</span><span class="token function">equals</span><span class="token punctuation">(</span>agent<span class="token punctuation">.</span>id_op<span class="token punctuation">)</span><span class="token punctuation">)</span> <span class="token punctuation">{</span>
    miAgente<span class="token punctuation">.</span>liberado <span class="token operator">=</span> <span class="token boolean">true</span><span class="token punctuation">;</span>
  <span class="token punctuation">}</span>
<span class="token punctuation">}</span>
<span class="token comment">// Recalcular condiciones del Hold</span>
hold_esperaSE<span class="token punctuation">.</span><span class="token function">recalculateConditions</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
<span class="token comment">// Reorganizar la cola</span>
queue_esperaSE<span class="token punctuation">.</span><span class="token function">sortAgents</span><span class="token punctuation">(</span><span class="token punctuation">)</span><span class="token punctuation">;</span>
</code></pre>
</li>
<li>
<p><strong>Comando para reordenar la cola de espera:</strong> Después de liberar una orden PT, es necesario asegurar que avance lo antes posible. Por defecto, las colas en AnyLogic operan bajo la disciplina FIFO (First In, First Out). Sin embargo, puede haber órdenes PT liberadas que estén detrás de órdenes PT no liberadas en la cola. Para evitarlo, se programa la lógica de ordenamiento de la cola para que dé prioridad a las órdenes <code>liberadas</code>. El siguiente código (simplificado) se utiliza en la acción “<code>On enter</code>” o “<code>On at exit</code>” de la cola para asignar una prioridad más alta a las órdenes liberadas (Condon et al., 2025, p. 52).</p>
<pre class=" language-java"><code class="prism  language-java"><span class="token comment">// Código para determinar la prioridad en la cola (simplificado)</span>
<span class="token keyword">return</span> agent<span class="token punctuation">.</span>liberado <span class="token operator">?</span> <span class="token number">2</span> <span class="token operator">:</span> <span class="token number">1</span><span class="token punctuation">;</span>
</code></pre>
</li>
</ul>
<h4 id="la-traza-como-comando-de-depuración">La traza como comando de depuración</h4>
<p>Además de los comandos de control, existen comandos para la verificación y depuración del modelo, conocidos como <strong>trazas</strong>. Durante la fase de construcción, los modeladores de Cambay insertaron líneas de código como <code>traceln()</code> en puntos clave del modelo para imprimir mensajes en la consola de AnyLogic. Esto les permitió seguir el rastro de las entidades, verificar los valores de los parámetros en cada paso y asegurarse de que la lógica programada se ejecutaba correctamente (Condon et al., 2025, p. 61). Por ejemplo, para ver qué mezcladora estaba tomando una orden:</p>
<pre><code>```java
traceln("La mezcladora 200 comenzó a procesar la orden OP" + agent);
```
</code></pre>
<p>En resumen, un modelo de simulación no es solo una colección de iconos, sino una compleja pieza de software. Su construcción requiere un profundo entendimiento del sistema real (modelo conceptual), una hábil utilización de las herramientas del software (estructura estática y dinámica) y la capacidad de programar la lógica de negocio mediante comandos, todo ello con el objetivo de crear una representación computacional válida y útil para la toma de decisiones (Condon et al., 2025, p. 83).</p>
<p><img src="image.png?ejemplos" alt=""> *<strong>Ejemplos de aplicación</strong></p>
<p><strong>Ejemplo 1 (Manufactura): Modelo computacional de una línea de ensamblaje</strong><br>
Una línea de ensamblaje con 5 estaciones de trabajo y 10 operarios puede modelarse en AnyLogic con la siguiente estructura:</p>
<ul>
<li><strong>Estructura estática:</strong> Layout de la línea con iconos para cada estación y un <code>ResourcePool</code> para los operarios.</li>
<li><strong>Estructura dinámica:</strong> Secuencia de bloques <code>Seize</code> (tomar un operario), <code>Delay</code> (tiempo de ensamblaje), <code>Release</code> (liberar operario) para cada estación.</li>
<li><strong>Comandos:</strong> Código Java para registrar el tiempo de ciclo de cada producto y generar informes al final de la simulación.</li>
</ul>
<p><strong>Ejemplo 2 (Logística): Modelo de un patio de maniobras</strong><br>
Un patio de maniobras con 3 grúas y espacio para 10 camiones puede modelarse así:</p>
<ul>
<li><strong>Estructura estática:</strong> Representación gráfica del patio con áreas de espera y zonas de carga/descarga. <code>ResourcePool</code> para las grúas.</li>
<li><strong>Estructura dinámica:</strong> <code>Source</code> genera camiones, <code>Seize</code> toma una grúa, <code>Delay</code> simula la carga/descarga (con tiempo variable según el tipo de carga), <code>Release</code> libera la grúa, <code>Sink</code> retira el camión.</li>
<li><strong>Comandos:</strong> Código para calcular estadísticas de utilización de grúas y tiempos de espera de camiones.</li>
</ul>
<p><strong>Ejemplo 3 (Cadena de Suministro): Modelo de un almacén con preparación de pedidos</strong><br>
Un almacén con 2 preparadores y una cinta transportadora puede modelarse con:</p>
<ul>
<li><strong>Estructura estática:</strong> Layout del almacén con estanterías, zona de picking y cinta transportadora. <code>ResourcePool</code> para los preparadores.</li>
<li><strong>Estructura dinámica:</strong> <code>Source</code> genera pedidos, <code>Seize</code> toma un preparador, <code>Delay</code> simula el tiempo de picking, <code>Release</code> libera el preparador, <code>Move To</code> traslada el pedido a la cinta, <code>Delay</code> simula el tiempo en cinta, <code>Sink</code> finaliza.</li>
<li><strong>Comandos:</strong> Código para asignar prioridades a pedidos urgentes y para registrar el tiempo total de preparación.</li>
</ul>
<p><img src="image.png?cierre_de_tema" alt=""> *<strong>Cierre</strong></p>
<p>Esta undécima semana ha completado el ciclo de modelación discreta de sistemas, demostrando cómo los conceptos teóricos se traducen en modelos computacionales funcionales. Se ha explorado la construcción de modelos en AnyLogic, diferenciando claramente entre estructura estática (los recursos y el layout) y estructura dinámica (el flujo de entidades y la lógica de eventos). Se han presentado los elementos básicos y avanzados del paquete de simulación, como los bloques <code>Seize</code>, <code>Delay</code>, <code>Release</code>, <code>SelectOutput</code> y <code>Hold</code>. Finalmente, se ha mostrado cómo los comandos en Java permiten extender la funcionalidad de estos bloques, programando lógica de negocio específica y facilitando la depuración del modelo. Con estos conocimientos, se está preparado para la última semana del curso, donde se integrarán todos los conceptos en un proyecto final que abarque desde la conceptualización hasta la recomendación de mejora basada en resultados de simulación.</p>
<p><img src="image.png?informaci%C3%B3n_complementaria" alt=""> *<strong>Información complementaria</strong></p>
<p>Se recomienda al estudiantado explorar los siguientes recursos para complementar su aprendizaje:</p>
<ul>
<li><strong>Tutoriales oficiales de AnyLogic:</strong> Disponibles en la página web de AnyLogic, cubren desde conceptos básicos hasta modelado avanzado.</li>
<li><strong>Foro de AnyLogic:</strong> Comunidad de usuarios donde se resuelven dudas y se comparten ejemplos de modelos.</li>
<li><strong>Video:</strong> “Advanced AnyLogic: Using Java Code in Your Models” (enlace en plataforma).</li>
<li><strong>Lectura complementaria:</strong> Manual de referencia de AnyLogic (disponible en formato PDF en el aula virtual).</li>
</ul>
<p><img src="image.png?referencias" alt=""> *<strong>Referencias</strong></p>
<p>Condon, C., López, P., &amp; Rius, A. (2025). <em>Simulación a Eventos Discretos para la Evaluación del Desempeño de Procesos Productivos</em> [Proyecto de Grado]. Universidad de la República.</p>
</div>
</body>

</html>
