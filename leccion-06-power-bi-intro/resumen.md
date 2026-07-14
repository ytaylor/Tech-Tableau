

# 📊 Módulo 4 – Lección 06: Introducción a Power BI


## 🔹 1. ¿Qué es Power BI?

Power BI es una herramienta de **análisis y visualización de datos** desarrollada por Microsoft que permite transformar datos en información visual interactiva 

### 🎯 ¿Por qué es importante?

* Fácil de usar (no requiere programación avanzada).
* Permite crear dashboards dinámicos.
* Se conecta a múltiples fuentes de datos.
* Facilita el trabajo colaborativo.
* Se integra con otras herramientas (Excel, Microsoft 365, etc.).

👉 Su objetivo principal es **convertir datos en decisiones**.

---

## 🔹 2. Blog Oficial de Power BI

El blog oficial es una fuente clave para mantenerse actualizado 

### 📌 ¿Qué encontramos allí?

* Actualizaciones mensuales.
* Nuevas funcionalidades.
* Buenas prácticas (DAX, modelado, visualización).
* Casos de éxito.
* Eventos y formaciones.

💡 Es recomendable revisar las **actualizaciones mensuales** para estar al día si trabajas con dashboards profesionales.

---

## 🔹 3. Interfaz de Power BI Desktop

Power BI Desktop se divide en varias vistas principales 

### 🧭 Menú superior

* **Archivo** → Abrir, guardar, publicar.
* **Inicio** → Obtener y transformar datos.
* **Vista** → Ajustes visuales.
* **Modelado** → Relaciones y medidas.
* **Insertar** → Imágenes y objetos.

---

### 🖥️ Vistas principales

#### 📊 Vista de Informe

* Crear y diseñar dashboards.
* Panel de campos.
* Panel de visualizaciones.
* Panel de filtros (nivel visual, página e informe).

#### 📄 Vista de Datos

* Ver tablas en formato tabular.
* Revisar estructura y contenido.

#### 🔗 Vista de Modelo

* Crear relaciones entre tablas.
* Configurar cardinalidad.

#### 🧠 Vista DAX Query

* Para usuarios avanzados.
* Permite analizar consultas DAX generadas por el motor.

---

## 🔹 4. Conexión de Ficheros

Power BI permite importar datos desde Excel, CSV, TXT y otras fuentes 

### 📂 Pasos básicos:

1. Inicio → Obtener datos.
2. Seleccionar tipo de archivo.
3. Cargar o Transformar datos.

---

### 🔗 Combinar ficheros (Merge)

Une tablas por columnas clave (como un JOIN en SQL).

Tipos de unión:

* Inner
* Left
* Right
* Full

---

### ➕ Concatenar ficheros (Append)

Une tablas por filas (misma estructura de columnas).

Muy útil para:

* Series temporales.
* Datos repartidos en varios archivos.

---

## 🔹 5. Transformación de Datos (Power Query)

La transformación se realiza en el **Editor de Power Query** 

Es un paso clave porque los datos rara vez vienen listos para analizar.

### 🎯 Objetivos:

* Limpiar errores.
* Homogeneizar formatos.
* Preparar datos para visualización.
* Mejorar rendimiento del modelo.

---

### 🔧 Transformaciones más importantes

* Filtrar filas
* Eliminar columnas
* Cambiar tipo de datos
* Dividir y combinar columnas
* Rellenar valores nulos
* Pivotar / Despivotar
* Agrupar por
* Crear columnas personalizadas
* Reemplazar valores
* Crear columnas condicionales
* Unir tablas
* Funciones geográficas
* Trabajar con fechas
* Web scraping básico

👉 Siempre finalizar con **Cerrar y aplicar**.

---

## 🔹 6. Configuración Regional, Fechas y Variables

Configurar correctamente el origen regional es clave al importar datos 

### 🌍 ¿Qué afecta?

* Formato de fechas (dd/mm vs mm/dd).
* Separador decimal.
* Delimitador de columnas.
* Codificación del archivo.

⚠️ Error común: que todo aparezca en una sola columna por mal delimitador.

---

### 🔢 Tipos de datos

Es fundamental revisar:

* Texto
* Número entero
* Decimal
* Fecha
* Fecha y hora
* Booleano
* Moneda

Errores frecuentes:

* Fechas mal interpretadas.
* Números como texto.
* Valores nulos.

---

## 📅 Jerarquía de Fechas

Power BI crea automáticamente jerarquías:

Año → Trimestre → Mes → Día

Permite:

* Análisis temporal dinámico.
* Navegación entre niveles.
* Mayor interactividad en gráficos.

💡 Buena práctica: usar tabla calendario para modelos más avanzados.
