
# 📊 Lección 03 · Personalización y Dashboards en Tableau

## 🎯 Objetivo 

En este bloque aprendemos a:

* Mejorar la claridad de nuestros gráficos.
* Diseñar visualizaciones más profesionales.
* Construir dashboards bien organizados.
* Aplicar buenas prácticas de diseño.
* Crear dashboards interactivos y publicarlos.

La idea es pasar de “hacer gráficos” a **diseñar experiencias visuales completas**.
--- 

# Graficos: 

## 📦 Hacer un boxplot

1. Arrastrar variable numérica a filas.
2. Convertir la variable a dimensión.
3. En las marcas → que sea un círculo.
4. Añadir línea de referencia sobre el eje.
5. Elegir diagrama de cuadro.
6. Girar el diagrama.

---

## 📊 Hacer un histograma

1. Arrastrar variable numérica a filas.
2. Elegir histograma.
3. Fijarse en la agrupación de la variable (bins).

---

---

## 📊 Gráficos con doble eje

Permiten mostrar dos métricas diferentes en el mismo gráfico.

Ejemplo:

* Ventas (€)
* Número de unidades

### Ventajas

* Comparar dos variables.
* Ahorrar espacio.
* Ver relaciones.

### Precauciones

* Deben tener sentido juntas.
* Usar colores distintos.
* No abusar del doble eje.

###  ✅ Crear ejes dobles

Pasos:

1. Poner la segunda métrica.
2. Convertir a eje doble.
3. Personalizar cómo se ven.
4. Sincronizar ejes.
5. Cuidado con las etiquetas.


---

# 🍩 Gráficos Donut

Un donut es un gráfico de pastel con un agujero en el centro.

Ese espacio central permite añadir:

* Un total.
* Una métrica clave.
* Un texto resumen.

---

## Cuándo usarlo

* Pocas categorías (2–5).
* Para mostrar partes de un todo.
* En dashboards ejecutivos.

## Cuándo evitarlo

* Muchas categorías.
* Comparaciones precisas.
* Valores muy similares.

👉 Si necesitas comparar con precisión, mejor usar barras.

## 🍩 Crear gráficos de donuts

1. Partiendo del grafico de barras.
2. Poner 1 dimensión.
3. Duplicar el 1.
4. Quitar todo al segundo.
5. Al 1º aumentar tamaño.

---

## Cómo crear un donut en Tableau

Tableau no lo tiene por defecto, pero se puede hacer:

1. Crear un gráfico de pastel.
2. Duplicarlo.
3. Convertir el segundo en un círculo pequeño.
4. Superponerlos en un dashboard.
5. (Opcional) Añadir un total en el centro.
---


# 🎨 Personalización de gráficos

Personalizar un gráfico no significa decorarlo.
Significa hacerlo **más claro y comprensible**.

---

## 🎨 Colores

El color ayuda a:

* Diferenciar categorías.
* Mostrar magnitudes con gradientes.
* Dirigir la atención.
* Mantener coherencia visual.

### Cómo cambiar colores

1. Arrastra un campo a la tarjeta **Color**.
2. Haz clic en la leyenda.
3. Selecciona **Editar colores**.
4. Elige una paleta adecuada.

### Buenas prácticas

* No uses demasiados colores.
* Evita colores muy parecidos.
* Usa paletas accesibles (Color Blind).
* Mantén coherencia entre gráficos.

👉 El color debe ayudar a leer, no distraer.

---

## 🏷️ Etiquetas y anotaciones

### Etiquetas

Muestran los valores exactos sobre el gráfico.

Se activan con:

* Clic derecho → Mostrar etiqueta de marca.

Útiles cuando:

* El número exacto es importante.
* Queremos dar precisión.

### Anotaciones

Sirven para explicar algo concreto en el gráfico.

Tipos:

* Punto
* Área
* Eje

Se usan para:

* Destacar un evento importante.
* Explicar un valor extraño.
* Añadir contexto.

👉 Las anotaciones convierten un gráfico en una historia.



## 🔺 Formas personalizadas

Permiten sustituir puntos por iconos.

Útiles en:

* Mapas.
* Gráficos narrativos.
* Dashboards visuales.

Consejos:

* No usar demasiadas formas.
* Mantener coherencia visual.

### 📁 Guradar formas en la carpeta documentos

* Mi repositorio Tableau.
* Formas.
* Crear carpeta con las imágenes.
---

---

# 📊 ¿Qué es un Dashboard?

Un dashboard es una pantalla que reúne varios gráficos en un solo lugar.

Sirve para:

* Mostrar información clave.
* Facilitar decisiones.
* Centralizar datos importantes.

No crea datos nuevos.
Organiza los gráficos existentes.

---

## Qué debe tener un buen dashboard

* Claridad.
* Jerarquía visual.
* Coherencia.
* Un objetivo definido.

👉 Un dashboard es una historia visual, no una colección de gráficos.

---

# 🧠 4. Antes de crear un dashboard

Antes de empezar, debemos responder:

## 1️⃣ ¿Cuál es el objetivo?

¿Qué queremos analizar o mejorar?

Ejemplo:

* Aumentar ventas.
* Reducir tiempos de respuesta.
* Analizar precios.

---

## 2️⃣ ¿Quién es la audiencia?

No es lo mismo un dashboard para:

* CEO
* Equipo técnico
* Marketing

Cada audiencia necesita métricas diferentes.

---

## 3️⃣ ¿Qué métricas incluir?

* Métricas de resultado (ventas, ingresos).
* Métricas accionables (lo que permite actuar).

Un buen dashboard permite tomar decisiones.

---

# 🎨 5. Consejos de diseño

* Diseña de izquierda a derecha.
* Coloca lo más importante arriba.
* Usa nombres claros.
* Mantén colores coherentes.
* No mezcles muchos marcos temporales.
* Agrupa métricas relacionadas.
* No satures con información.

👉 Si un dato no aporta valor, elimínalo.

Usa la metodología de diseño de S.C.R.A.P

![](scrap.jpeg)

---

# 📐 6. Estructura del Dashboard

## Tamaño

Opciones:

* Fijo → Presentaciones.
* Automático → Web.
* Rango → Intermedio.

Recomendación habitual:
1200x800 como base.

---

## 🧩 Objetos: Mosaico vs Flotantes

### Mosaico (Tiled)

* Alineación automática.
* Diseño limpio.
* Mejor para dashboards responsivos.

### Flotantes (Floating)

* Posición libre.
* Permite superponer elementos.
* Más creativo, pero menos estable.

👉 Recomendación: usar mosaico como base y flotantes solo cuando sea necesario.

---

## 📦 Contenedores

Permiten:

* Agrupar elementos.
* Alinear automáticamente.
* Crear secciones organizadas.

Tipos:

* Vertical
* Horizontal

👉 Usar contenedores ayuda a mantener orden.

---

# 🚀 7. Crear un Dashboard paso a paso

1. Crear visualizaciones individuales.
2. Crear nuevo dashboard.
3. Definir tamaño.
4. Arrastrar hojas.
5. Organizar con mosaico o flotante.
6. Añadir filtros.
7. Añadir acciones (interactividad).
8. Ajustar estilo.
9. Publicar.

---


# Elementos Visuales en Dashboards

Mejoran navegación, estética y experiencia de usuario.

---

## 🖼 Imágenes

Sirven para:

* Logos.
* Encabezados.
* Contexto visual.

Se añaden desde:
**Objetos → Imagen**

Recomendación:

* Usar PNG o JPG optimizados.

---

## 🔘 Botones de navegación

Permiten:

* Ir a otra hoja.
* Ir a otro dashboard.
* Crear menús.

Se crean desde:
**Objetos → Botón de navegación**

Útiles para:

* Crear estructura tipo web.
* Añadir botón “volver atrás”.

---

## 👁 Botón mostrar/ocultar

Permite:

* Mostrar filtros avanzados.
* Ocultar paneles.
* Hacer dashboard más limpio.

Pasos:

1. Agrupar elementos en contenedor.
2. Activar "Agregar botón mostrar/ocultar".

---

## 📝 Textos

Sirven para:

* Títulos.
* Subtítulos.
* Instrucciones.

Buenas prácticas:

* Textos breves.
* Claros.
* No saturar.

---
# 🌍 Publicar en Tableau Public

Permite:

* Compartir dashboards.
* Crear portfolio.
* Obtener enlace público.
* Incrustar en web.

⚠️ Todo lo que se publica es público.
No usar datos sensibles.