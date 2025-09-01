### <span class="text-primary">Módulo 2:</span><br> Prompt Engineering 🚀✨

- 🏗️ Los 4 Pilares de un Prompt  <!-- .element: class="fragment" data-fragment-index="1" -->
- 🧠 Técnicas Fundamentales:<!-- .element: class="fragment" data-fragment-index="2" --> <b class="text-primary">Zero-shot</b><!-- .element: class="fragment" data-fragment-index="2" -->, <b class="text-primary">Few-shot</b><!-- .element: class="fragment" data-fragment-index="2" -->, <b class="text-primary">Chain-of-Thought</b><!-- .element: class="fragment" data-fragment-index="2" -->, <b class="text-primary">Tree-of-Thoughts</b><!-- .element: class="fragment" data-fragment-index="2" -->
- 📝 Uso de formatos para mejorar la precisión y el contexto  <!-- .element: class="fragment" data-fragment-index="4" -->



### Los 4 Pilares de un Prompt 🏗️

- <b class="text-primary">Rol:</b> ¿Quién debe ser la IA?
- <b class="text-primary">Contexto:</b> ¿Por qué se realiza la tarea?
- <b class="text-primary">Tarea:</b> ¿Qué acción debe ejecutar?
- <b class="text-primary">Formato:</b> ¿Cómo debe ser la respuesta?


### Estructuras de un Prompt 🧩

<img src="./assets/images/module-2/prompt-schemas.png" alt="esquemas de prompts" style="height:400px" />


#### Ejemplo: T-A-O

![tao](./assets/images/module-2/esquema-t-a-o.png)

note:
Necesito ideas para el lanzamiento de un nuevo producto lácteo.

Genera 3 nombres para un nuevo yogur con probióticos.

El nombre debe comunicar bienestar digestivo y ser fácil de recordar para las familias.


#### Ejemplo: R-T-F

![rtf](./assets/images/module-2/esquema-r-t-f.png)

note:
Eres un especialista en sistemas de gestión de calidad e inocuidad alimentaria.

Redacta un borrador del objetivo para un nuevo procedimiento de limpieza y desinfección en la planta.

La respuesta debe ser un único párrafo de no más de 50 palabras.


#### Ejemplo: B-A-B

![rtf](./assets/images/module-2/esquema-b-a-b.png)

note:
El equipo de I+D invierte mucho tiempo buscando manualmente nuevas tendencias en ingredientes y productos lácteos a nivel mundial.

Queremos que el equipo reciba un resumen mensual con las innovaciones más relevantes para inspirar la creación de nuevos productos.

Diseña la estructura de un prompt que pueda usarse mensualmente para solicitar a ChatGPT este resumen de tendencias del sector lácteo.


#### Ejemplo: C-A-R-E

<img src="./assets/images/module-2/esquema-c-a-r-e.png" alt="esquema C-A-R-E" style="height:450px" />

note:
Somos Fasalact S.A.S. y necesitamos crear contenido para nuestro blog corporativo para atraer a clientes B2B (empresas).

Escribe un párrafo introductorio para un artículo titulado "La Importancia de la Leche de Alta Calidad como Materia Prima".

El párrafo debe ser profesional, resaltar nuestro compromiso con la calidad desde el origen y captar el interés de gerentes de producción o desarrollo de otras empresas.

Un buen inicio sería: "En la industria de alimentos, el producto final es un reflejo directo de sus ingredientes. Para nosotros en Fasalact, todo comienza con una materia prima insuperable: la leche. Pero, ¿qué define realmente una leche de 'alta calidad' y por qué es el pilar de la innovación y seguridad en sus productos?".



### Técnicas de Prompt Engineering 🛠️

- <b class="text-primary">Zero-shot 🎯</b> 
- <b class="text-primary">Few-shot 📚</b> 
- <b class="text-primary">Chain-of-Thought 🧠➡️</b>
- <b class="text-primary">Tree-of-Thoughts 🌳➡️</b>


### <span class="text-primary">Zero-shot</span> 🎯

Consiste en pedirle al modelo que haga una tarea solo con la instrucción, sin ejemplos.

<b class="text-primary">Úsalo:</b> Para tareas simples que el modelo ya conoce, como traducir, resumir o clasificar sentimientos.
<!-- .element: class="fragment" data-fragment-index="1" -->

note:
Es la forma más simple y directa de interactuar con un LLM.

Gracias a su vasto entrenamiento, entienda y la ejecute correctamente.

**Analogía:** Es como pedirle a un chef experimentado que te prepare un "omelette" sin darle la receta. Asumes que ya sabe lo que es y cómo hacerlo.

**Ejemplo:** Clasifica el siguiente comentario de un cliente en una de estas tres categorías: "Calidad", "Sugerencia de Producto" o "Marketing".

Comentario a analizar:
"Hola, me encanta su nuevo kefir de Arandanos, pero la textura se sentía un poco más espesa esta vez. ¿Han considerado lanzar una opción más ligera? Sería increíble."


### <span class="text-primary">Few-shot</span> 📚

Consiste en mostrarle al modelo algunos ejemplos de lo que esperas como entrada y salida.

<b class="text-primary">Úsalo:</b> Cuando la tarea es más compleja, requiere un formato específico o buscas mayor control en la respuesta.
<!-- .element: class="fragment" data-fragment-index="1" -->

note:
Permite guiar al modelo con ejemplos concretos, mejorando la precisión y el estilo de la respuesta.

**Analogía:** Es como pedirle a un chef un platillo y mostrarle fotos de cómo quieres que se vea el resultado final.

**Ejemplo:**
Redacta una descripción breve para la etiqueta del nuevo producto, siguiendo el estilo y formato de los ejemplos.

**Ejemplo 1:**
Producto: Yogurt Griego Sabor Vainilla
Descripción:
Cremoso y refrescante. Nuestro Yogurt Griego Sabor Vainilla está elaborado con leche fresca y fermentos naturales para cuidar tu digestión.
Ideal para: Acompañar tus desayunos.
Atributos: #Tradicional #Saludable #Cremoso

**Ejemplo 2:**
Producto: Queso Cottage
Descripción:
Suave y cremoso. Nuestro Queso Cottage está hecho con leche fresca y es perfecto para añadir a tus ensaladas o disfrutar solo.
Ideal para: Postres y antojos.
Atributos: #Artesanal #Clásico #Dulce

**Nuevo Producto:**
Producto: Yogur Griego con Miel y Nueces
Características: Alto en proteína, cremosidad extra, endulzado naturalmente con miel.
Descripción:


### <span class="text-primary">Chain-of-Thought</span> 🧠➡️

Consiste en pedirle al modelo que explique su razonamiento paso a paso antes de dar la respuesta final.

<b class="text-primary">Úsalo:</b> Para problemas que requieren lógica, cálculos o varios pasos para llegar a la solución.
<!-- .element: class="fragment" data-fragment-index="1" -->

note:
Obligar al modelo a "pensar en voz alta" ayuda a obtener respuestas más precisas y fundamentadas.

**Analogía:** Es como resolver un problema de matemáticas mostrando todos los pasos, no solo la respuesta final.

**Ejemplo:**
**Contexto:**
Actúa como jefe de compras en Fasalact S.A.S. Debes seleccionar un proveedor de un nuevo cultivo probiótico para el lanzamiento de un yogur premium. La prioridad inicial es la flexibilidad y minimizar el riesgo, ya que es un producto nuevo y no conocemos la demanda. El costo por volumen se volverá más importante en 6 meses si el producto tiene éxito.

**Datos de los Proveedores:**

* **Proveedor A (ProbioGlobal):**
    * Costo: 250.000 COP por kg.
    * Pedido Mínimo (MOQ): 100 kg.
    * Tiempo de entrega: 15 días.
    * Certificaciones: HACCP.
    * Reputación: Líder del mercado, muy confiable pero poco flexible.

* **Proveedor B (InnovaCultures):**
    * Costo: 290.000 COP por kg.
    * Pedido Mínimo (MOQ): 20 kg.
    * Tiempo de entrega: 7 días.
    * Certificaciones: HACCP y Certificación Orgánica.
    * Reputación: Proveedor más nuevo pero con excelentes referencias en productos innovadores.

**Instrucción:**
Analiza la situación paso a paso para decidir qué proveedor contratar para la fase de lanzamiento. Tu análisis debe incluir:

1.  Una evaluación de los pros y contras de cada proveedor *específicamente para nuestra prioridad actual* (flexibilidad y bajo riesgo).
2.  Un cálculo del costo de inversión inicial para el pedido mínimo de cada uno.
3.  Una recomendación final justificada que explique por qué un proveedor es mejor que el otro para esta etapa inicial.



### Marcado de texto (<span class="text-primary">Markdown</span>) 📝

- Lenguaje ligero para dar formato legible: encabezados, listas, enlaces y énfasis. <!-- .element: class="fragment" data-fragment-index="1" -->
- En prompts, ayuda a estructurar instrucciones y salidas con claridad y consistencia. <!-- .element: class="fragment" data-fragment-index="2" -->
- Separa contenido de presentación: te enfocas en qué decir, no en cómo se ve. <!-- .element: class="fragment" data-fragment-index="3" -->
- Pide el formato deseado (listas, tablas o secciones) para respuestas más precisas. <!-- .element: class="fragment" data-fragment-index="4" -->

note:
Usa Markdown para definir plantillas de salida: títulos H2, secciones numeradas, listas de verificación o tablas. Esto reduce ambigüedad y facilita evaluación y reutilización.


<!-- .slide: data-background-iframe="https://markdownlivepreview.com/" -->



### <span class="text-primary">Tree of Thoughts</span> (ToT) 🌳🧠

- Técnica para explorar varias líneas de razonamiento en paralelo.
- En lugar de un camino lineal (CoT), organiza ideas como un árbol con ramas.
- Útil para planificación, estrategia, acertijos y escritura creativa.

note:
ToT permite que el modelo considere múltiples rutas, compare y elija la mejor.
Frente a CoT (lineal), ToT eleva la probabilidad de buenas soluciones en problemas complejos.


### Cómo funciona ToT ⚙️

1. Genera posibles pasos/ideas a ejecutar.
2. Evalúa cada idea.
3. Descartar ideas que no son óptimas y desarrolla las prometedoras.
4. Itera hasta resolver o alcanzar límites

note:
🌳 Piensa en un árbol de decisiones: explorar → evaluar → podar.
Criterios típicos: puntaje del modelo, límite de profundidad/ancho, tiempo o confianza.

Destaca el patrón: generar → evaluar → retroceder/seleccionar.
Aplica a acertijos, planificación, código y contenido creativo.
Tip: si el tiempo es limitado, reduce profundidad o ancho; usa una evaluación heurística simple (1–10).

**Ejemplo:**
**Objetivo:** Diseñar y seleccionar la estrategia de marketing más efectiva para aumentar el consumo del yogur griego *Sketos* entre jóvenes de 18 a 25 años.

**Instrucciones:**

1. **Genera 3 estrategias de marketing distintas** enfocadas en el público objetivo (jóvenes de 18 a 25 años).

2. Para **cada estrategia**, incluye:

   * **Resumen de la idea** (máximo 40 palabras).
   * **Canales clave a utilizar** (p. ej.: TikTok, Instagram, punto de venta, colaboraciones con influencers).
   * **Riesgos principales** (p. ej.: alto costo, baja interacción, saturación del canal).
   * **Evaluación del impacto potencial** (califica de 1 a 10 según tu estimación de efectividad, considerando factores como viralidad, conexión con el público objetivo, escalabilidad y costo; justifica el valor dado).
   * **Breve análisis de ROI estimado** (retorno en relación con la inversión).

3. **Condición de backtracking:**
   Si **ninguna estrategia obtiene una puntuación mayor a 7**, elige la mejor valorada, propón una **versión mejorada de esta estrategia** (ajusta el enfoque, canal, mensaje u otros elementos clave), y vuelve a evaluarla.

4. **Selección final:**
   Elige la estrategia con **el mayor puntaje final** y justifica tu elección basándote en:

   * Su potencial de ROI.
   * Nivel de alineación con la marca Sketos (identidad, valores, estilo).
   * Relevancia cultural para el público objetivo.

**Formato de salida esperado:**

* Muestra el razonamiento implementado
* Lista numerada de estrategias (máximo 5).
* Evaluación completa de cada una.
* Estrategia final seleccionada con su justificación clara.



## ¡Gracias!

note:
💬 Agradece y abre espacio para preguntas y discusión.