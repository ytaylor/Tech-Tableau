
# 📊 Resumen – Gráficas en Power BI
## 1️⃣ Introducción a gráficos en Power BI 

Para crear visualizaciones en Power BI seguimos estos pasos:

1. **Importar datos**

   * Inicio → Obtener datos.
   * Elegir fuente (Excel, CSV, SQL, etc.).
   * Los campos aparecen en el panel derecho.

2. **Transformar datos (opcional)**

   * Transformar datos → Editor de Power Query.
   * Limpiar, cambiar tipos, renombrar columnas.
   * Cerrar y aplicar.

3. **Crear gráfico en Vista de Informe**

   * Elegir tipo de visualización primero.
   * Arrastrar campos a:

     * **Eje**
     * **Valores**
     * **Leyenda**
     * **Filtros**

🔎 Diferencia con Tableau: en Power BI primero eliges la visualización y después arrastras los campos.

---

## 2️⃣ Tipos de gráficos 

Power BI ofrece muchas visualizaciones:

* 📊 **Barras / Columnas** → Comparar categorías.
* 📈 **Líneas** → Tendencias en el tiempo.
* 🥧 **Pie (Quesito)** → Parte de un total.
* 📍 **Dispersión (Scatter)** → Relación entre variables.
* 🌊 **Área** → Evolución con magnitud.
* 📊 **Histograma** → Distribución de datos.
* 🗺 **Mapas** → Datos geográficos.
* 🔵 **Burbujas** → Relación entre 3 variables.
* 🎯 **KPI** → Métricas clave.
* 🧾 **Matriz** → Tabla con agregaciones.

También se pueden añadir gráficos adicionales desde el marketplace.

---

## 3️⃣ Creación de gráficos 

Ejemplo práctico (ventas por estado):

1. Seleccionar gráfico (ej. columnas).
2. Arrastrar dimensión al eje X.
3. Arrastrar métrica al eje Y.
4. Ajustar agregación (suma, promedio, etc.).
5. Aplicar filtros si es necesario.
6. Formatear colores, ejes, etiquetas.

💡 Se puede cambiar el tipo de gráfico sin perder los campos arrastrados.


## 4️⃣ Mapas en Power BI 

### Tipos:

* 🗺 Mapa básico
* 🧩 Shape Map (mapa de formas)
* ☁ Azure Maps

### Requisitos:

* Columnas geográficas (ciudad, país, CP, coordenadas).
* Configurar categoría de datos correctamente.

### Buenas prácticas:

* Evitar ambigüedades (ej. varias ciudades con mismo nombre).
* No saturar el mapa.
* Usar filtros para claridad.

---

## 5️⃣  Eje secundario 

### 📊 Eje secundario

Se usa cuando hay dos métricas con escalas muy diferentes.

Ejemplo:

* Columnas → Ventas
* Línea → Nº clientes (con eje secundario)

Se usa un **gráfico combinado** y se activa la opción de eje secundario.

---

## 6️⃣ Filtros y Segmentos (Slicers) 

### 🎛 Segmentos (Slicers)

Filtros visuales e interactivos.

Tipos:

* Lista
* Rango de fechas
* Jerárquico
* Numérico

Ventajas:

* Muy intuitivos.
* Ideales para dashboards dinámicos.

Pueden aplicarse a:

* Visual
* Página
* Informe completo (sincronizados)

---

### ⚖️ Filtros

Más técnicos y precisos.

Tipos:

* Nivel visual
* Nivel página
* Nivel informe

Ventajas:

* Mayor control.
* Permiten condiciones complejas.
* No visibles por defecto.

---

### 🔄 Diferencia clave

| Filtros         | Segmentos         |
| --------------- | ----------------- |
| Más técnicos    | Más visuales      |
| Invisibles      | Siempre visibles  |
| Mayor precisión | Mayor interacción |

💡 Recomendación: combinar ambos.

---

## 7️⃣ Uso compartido 

Power BI Desktop es para crear, no para compartir directamente.

Opciones:

* 📁 Compartir archivo `.pbix`
* 📄 Exportar a PDF
* 📊 Exportar a PowerPoint
* ☁ Publicar en Power BI Service (online)

También:

* Se pueden copiar y pegar visuales.
* Guardar como `.pbix`.
* Publicar en la nube para colaboración.

--