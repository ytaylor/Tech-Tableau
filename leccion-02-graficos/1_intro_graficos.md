# 🗺️ Gráficos en Tableau

##  1 · ¿Qué es un gráfico y para qué sirve?
Un gráfico no es una imagen bonita, es una representación visual diseñada para comunicar información de forma clara y eficiente.
- El cerebro procesa imágenes más rápido que tablas.
- Un gráfico correcto reduce la carga cognitiva.
- Un gráfico mal elegido puede generar interpretaciones erróneas.
- Un gráfico es una representación visual para:
  - detectar patrones,
  - comparar valores,
  - entender tendencias.
- Un buen gráfico comunica rápido.
- Un mal gráfico confunde, aunque los datos sean correctos.

##  2 · Medidas y dimensiones (la base de TODO)

En Tableau todo gráfico es: Dimensión + Medida agregada

### Dimensiones (azul)
- Categorizan
- Segmentan
- Dividen el análisis

Ejemplos:
- Región
- Año
- Categoría

### Medidas (verde)
- Son valores numéricos
- Se agregan
- Representan magnitudes

Ejemplos:
- Ventas
- Precio
- Cantidad

---

##  3 · Hoja de trabajo de Tableau

- Cada hoja es una representacion unica de una visualizacion
- Hay que hacer que cada hoja tenga un nombre
- Un dashboard = combinación de hoja

## Lógica visual

- Panel izquierdo → datos disponibles
- Columnas y filas → estructura del gráfico
- Marcas → estética y detalle
- Filtros → control
- Mostrarme → sugerencias, no decisiones automáticas
---

### 🧠 Zonas principales
- **Panel de datos**: campos disponibles
- **Columnas y Filas**: estructura del gráfico
- **Marcas**:
  - color
  - tamaño
  - etiqueta
  - detalle
- **Filtros**: limitar los datos
- **Mostrarme**: sugerencias de gráficos posibles

📌 **Idea clave**
Cada hoja de trabajo = **un gráfico**.

---

##  4 · Tipos de gráficos y cuándo usarlos

### 🧠 Gráficos principales

## Barras
Para comparar categorías.
Muy intuitivas.
Primera opción casi siempre.

> “Si comparo categorías, uso barras.”

## Líneas
Para evolución temporal.
Necesitan fecha continua para conectar puntos.

> “Si quiero ver tendencia, uso línea.”

## Dispersión
Para analizar relación entre dos variables numéricas.
Requiere mayor madurez analítica.

## Pastel
Solo si hay pocas categorías.
Mejor usar barras casi siempre.

## Tabla
Para detalle.
No debe saturarse.

📌 **Regla de oro**
> El gráfico depende de la pregunta, no del gusto personal.

---

##  5 · Agregaciones: cómo se resumen los datos

Agregar es cambiar el nivel de detalle.
- Tengo 1.000 reservas.
- ¿Quiero ver cada reserva?
- ¿O quiero el total por año?

SUM, AVG, COUNT, COUNTD, MIN, MAX.

- Tableau agrega por defecto.
- Siempre revisar qué agregación está usando.

> “La pregunta determina la agregación.”


### 🧠 Funciones habituales
- `SUM()` → total
- `AVG()` → media
- `COUNT()` → número de filas
- `COUNTD()` → valores únicos
- `MIN()` / `MAX()`

📌 **Ejemplo**
- Precio medio por barrio = `AVG(price)`
- Número de alojamientos = `COUNT(id)`

⚠️ **Error típico**
No revisar qué agregación está usando Tableau por defecto.

✅ **Qué deberías saber hacer**
Cambiar y justificar la agregación de una medida.

---

##  6 · Fechas en Tableau: discretas vs continuas

Este es un punto crítico para evitar frustraciones.

Fecha discreta (azul):
- Categorías separadas.
- Comparación de periodos.

Fecha continua (verde):
- Línea temporal real.
- Tendencias.

## Problemas habituales

- Línea que no conecta → fecha discreta.
- Meses que desaparecen → uso incorrecto.


> “Si quiero tendencia, fecha continua.”

---

##  7 · Uso del color como dimensión

Usar el color para comunicar, no para decorar.

### 🧠 Buen uso del color
- Color para **categorías**
- Pocas categorías (2–6)
- Buen contraste
- Paletas accesibles

### ❌ Mal uso del color
- Color sin significado
- Demasiados colores
- Colores difíciles de distinguir

> “El color comunica. Si no comunica, sobra.”


---
