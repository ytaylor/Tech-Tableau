
# 🎨 Accesibilidad y Daltonismo en Visualización de Datos

Hasta ahora hemos hablado de tipos de gráficos, agregaciones, fechas y color.  
Pero hay algo igual de importante que muchas veces se pasa por alto: la accesibilidad.

Cuando creamos un dashboard, no lo hacemos para nosotros.  
Lo hacemos para otras personas.

Si una parte de nuestro público no puede interpretar correctamente lo que mostramos, entonces el gráfico falla, aunque técnicamente esté bien construido.

Por eso, hablar de accesibilidad no es un tema opcional.  
Es parte del diseño responsable.

---

## 👁️ ¿Qué es el daltonismo?

El daltonismo es una alteración en la percepción del color.

No significa que la persona vea en blanco y negro.  
Significa que tiene dificultad para distinguir ciertos colores.

El tipo más común es el daltonismo rojo-verde.

Esto implica que:
- El rojo puede parecer marrón o gris.
- El verde puede parecer muy similar al rojo.
- Ambos pueden verse prácticamente iguales.

Y esto no es algo raro.

Aproximadamente:
- 1 de cada 12 hombres tiene algún tipo de daltonismo.
- 1 de cada 200 mujeres también.

Eso significa que en cualquier grupo de trabajo, clase o empresa, probablemente haya alguien que no perciba los colores como nosotros.

---

## ⚠️ El error más común en dashboards

Uno de los errores más habituales en visualización es usar:

- Verde para indicar algo positivo.
- Rojo para indicar algo negativo.

Por ejemplo:
- Verde → beneficios.
- Rojo → pérdidas.

El problema es que para una persona con daltonismo rojo-verde, ambos colores pueden parecer muy similares.

Si el significado del gráfico depende únicamente del color, entonces esa persona no puede interpretarlo correctamente.


> Si el significado depende solo del color, el gráfico no es accesible.

---

## 🎨 El color no es decoración

En Tableau, cuando arrastramos una dimensión al estante de Color, estamos haciendo una decisión visual importante.

El color se convierte en una variable que transmite información.

No es algo estético.
No es algo decorativo.
Es una codificación visual.

Eso significa que debe tener una intención clara y una función comunicativa.

Antes de usar color, debemos preguntarnos:

- ¿Estoy usando color para diferenciar categorías?
- ¿Es realmente necesario?
- ¿Se entendería igual si lo imprimo en blanco y negro?

Si la respuesta es no, probablemente el gráfico dependa demasiado del color.

---

## ✅ Buenas prácticas para visualizaciones accesibles

### 1️⃣ Usar paletas accesibles

Tableau incluye paletas diseñadas específicamente para personas con daltonismo.

Por ejemplo:
- Color Blind
- Color Blind 10
- Azul-Naranja

Estas paletas están pensadas para tener alto contraste y buena diferenciación.

Siempre que usemos color para categorías importantes, es recomendable revisar estas opciones.

---

### 2️⃣ No depender únicamente del color

El color puede reforzar un mensaje, pero no debe ser el único canal.

Podemos añadir:
- Etiquetas numéricas.
- Iconos.
- Formas distintas.
- Diferencias en tamaño.
- Líneas discontinuas frente a continuas.

Por ejemplo:
En lugar de usar solo rojo y verde para indicar subida o bajada, podemos añadir:

- Flechas ↑ ↓
- Texto que indique “+12%” o “-8%”
- Iconos junto al valor

Esto hace que el gráfico sea comprensible incluso si alguien no distingue los colores.

---

### 3️⃣ Mantener buen contraste

No todos los problemas son de daltonismo.

También debemos cuidar:

- Que el texto no sea gris claro sobre fondo blanco.
- Que los colores no sean demasiado similares.
- Que el tamaño de letra sea suficiente.
- Que el fondo no distraiga.

Un gráfico puede ser visualmente atractivo pero ilegible.

La claridad siempre está por encima de la estética.

---

### 4️⃣ Evitar exceso de colores

Cuantos más colores usamos, más difícil es interpretarlos.

Lo recomendable es:
- Entre 2 y 6 categorías como máximo.
- Más de eso genera saturación visual.

Si necesitamos más categorías:
- Quizá debemos cambiar el tipo de gráfico.
- O usar filtros.
- O dividir en varias visualizaciones.

---

## 🧠 Reflexión

Diseñar dashboards no es solo una cuestión técnica.  
Es una cuestión de responsabilidad.

Cuando trabajamos con datos:
- Estamos comunicando información.
- Estamos ayudando a tomar decisiones.
- Estamos influyendo en cómo se interpreta una realidad.

Por eso, debemos asegurarnos de que nuestro mensaje sea claro para el mayor número de personas posible.

---

> Un buen dashboard no solo comunica datos.  
> Comunica datos a todas las personas.

