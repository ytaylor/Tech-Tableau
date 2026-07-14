# 📊 Resumen – Dashboards en Power BI
---

## 1️⃣ Introducción: Página, Informe y Dashboard 

Antes de crear dashboards es importante distinguir:

* **Página** → Una vista dentro de un informe donde se organizan visualizaciones relacionadas.
* **Informe** → Archivo `.pbix` creado en Power BI Desktop que contiene una o varias páginas con gráficos y análisis.
* **Dashboard** → Panel interactivo que reúne visualizaciones clave. Se crea en Power BI Service (entorno online).

📌 En este módulo trabajamos en **Power BI Desktop**, aunque llamemos “dashboard” al informe.

---

## 2️⃣ ¿Qué es un Dashboard en Power BI? 

Un dashboard es una **vista visual e interactiva** que resume datos clave para facilitar la toma de decisiones rápidas.

En Power BI:

* Se pueden incluir **varias visualizaciones en una misma página**.
* Permite combinar gráficos, KPIs, tablas, mapas y filtros.

---

### 🛠 Pasos para crear un informe tipo dashboard

1. **Conectar datos**
2. **Transformar (si es necesario)**
3. **Crear visualizaciones**
4. **Organizar páginas**
5. **Configurar interactividad**
6. **Diseñar y formatear**
7. **Revisar y guardar (.pbix)**

---

## 🧱 Componentes principales de un Dashboard

Un dashboard bien estructurado incluye:

### 📌 1. Título principal

* Claro y directo.
* Ubicado en la parte superior.

### 📅 2. Segmentadores (Slicers)

* Permiten filtrar por:

  * Fecha
  * Región
  * Producto
  * Cliente
* Se colocan arriba o a la izquierda.

### 📊 3. Gráficos clave

* KPI Cards (métricas principales)
* Gráficos de columnas o barras
* Líneas (tendencias)
* Mapas (si aplica)
* Tablas o matrices

✅ Variedad sin sobrecargar.

---

## 3️⃣ Interacciones entre visualizaciones 

Power BI permite controlar cómo interactúan los gráficos entre sí.

Opciones disponibles:

### 🔍 Filtrar

Solo muestra los datos relacionados con la selección.

👉 Ideal para análisis detallado.

---

### 🌟 Resaltar

Mantiene todos los datos visibles pero destaca la parte seleccionada.

👉 Ideal para mantener contexto.

---

### 🚫 Ignorar

La visualización no se ve afectada por otras selecciones.

👉 Útil para KPIs fijos o comparativas.

---

### Cómo configurarlo:

1. Seleccionar visual.
2. Ir a **Formato → Editar interacciones**.
3. Elegir comportamiento en cada visual.

---

## 4️⃣ Diseño visual del dashboard 

El diseño es clave para la comprensión y experiencia del usuario.

---

### 🧾 Tooltips (Información emergente)

Permiten mostrar información adicional al pasar el ratón.

Se pueden:

* Activar en el panel de formato.
  - Formato - > Permitir el uso como información sobre herramientas 
  - Decidir que campo vamos a usar para que se active el Tooltip y arrastrarlo. 
  - Crear el grafico que se va a usar como tooltip.

  - Ocultar la hoja
  -  En el grafico que se va a usar como tooltip, en formato, activar la opción de tooltip personalizado y seleccionar el grafico creado: General -> Información sobre herramientas -> Tipo de información sobre herramientas personalizada -> Seleccionar el grafico creado.
* Crear páginas específicas como tooltip personalizados.

💡 Ideal para mostrar detalles sin sobrecargar el dashboard.

---

### 🎚 Sliders (Controles deslizantes)

Permiten filtrar por rangos (fechas, números).

Se crean usando un **segmentador** con formato de rango.

---

### 🎨 Personalización visual

Se puede modificar:

* Colores (incluyendo colores condicionales)
* Títulos
* Fondos y bordes
* Sombras y efectos
* Tamaño y posición

---

### ✅ Buenas prácticas de diseño

* Mantener coherencia de colores.
* No sobrecargar de gráficos.
* Usar tooltips estratégicamente.
* Cuidar accesibilidad (contraste, tamaño de texto).
* Crear jerarquía visual clara.

---

## 5️⃣ Parámetros, Grupos y Columnas Condicionales 

Estas herramientas permiten hacer dashboards más dinámicos y estructurados.

---

### 🎯 Parámetros

Son variables reutilizables que permiten:

* Cambiar rutas de archivos.
* Filtrar datos dinámicamente.
* Hacer el informe más flexible.

Se crean en:
Inicio → Transformar datos → Administrador de parámetros.

---

### 🧩 Agrupar datos (Group By)

Funciona como un `GROUP BY` en SQL.

Permite:

* Sumar ventas por categoría.
* Contar clientes.
* Calcular promedios.

Se usa desde Power Query con la opción **Agrupar por**.

---

### 🧠 Columna condicional

Permite crear reglas tipo:

* Si ventas > 1000 → “Alta”
* Si ventas < 500 → “Baja”

Se crea desde:
Power Query → Agregar columna → Columna condicional.

---

### 💡 En resumen:

Un buen dashboard en Power BI debe ser:

* Claro
* Interactivo
* Visualmente coherente
* Orientado a la toma de decisiones
* Bien estructurado
