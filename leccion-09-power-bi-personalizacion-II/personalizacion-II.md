
# 📊 Personalización de Dashboards en Power BI

En esta lección se aprende a enriquecer informes mediante visualizaciones analíticas y herramientas avanzadas de navegación .

## 1️⃣ Visualizaciones Analíticas

### 🔹 Histograma

Power BI **no tiene un histograma nativo**, pero se puede crear de dos formas :

* **Opción A:** Importar visualización personalizada desde el marketplace. (Solo si tienes cuenta corporativa).
* **Opción B:** Simularlo con un gráfico de columnas agrupadas creando una columna de intervalos (bins) con DAX.

Ejemplo de agrupación:

```
RangoEdad = INT('Clientes'[Edad]/10)*10
```

📌 El histograma permite visualizar la **distribución de una variable numérica**.

---

### 🔹 Scatter Plot (Diagrama de dispersión)

Se utiliza para analizar la relación entre dos variables numéricas .

Configuración básica:

* Eje X → Variable numérica
* Eje Y → Otra variable numérica
* Tamaño (opcional) → Medida adicional
* Leyenda (opcional) → Variable categórica

📌 Permite detectar **correlaciones, patrones y concentraciones**.

---

## 2️⃣ Organización y Diseño del Dashboard

Se trabajan buenas prácticas de diseño :

* Jerarquía visual clara (título → KPIs → gráficos → filtros).
* Distribución ordenada y alineada.
* Enfoque en la toma de decisiones.
* Uso coherente de colores y espacios.

El objetivo es crear dashboards claros, estructurados y profesionales.

---

## 3️⃣ Marcadores (Bookmarks)

Los **marcadores** permiten guardar el estado de una página :

* Filtros aplicados
* Visibilidad de objetos
* Selecciones activas
* Posición del scroll

### Usos principales:

* Cambiar entre vistas
* Mostrar/ocultar visualizaciones
* Simular pestañas
* Crear navegación personalizada

Se pueden configurar para recordar:

* Datos
* Visuales
* Foco y selección

Son clave para hacer dashboards dinámicos sin cambiar de página.

---

## 4️⃣ Botones Interactivos

Los **botones** permiten ejecutar acciones con un clic :

### Acciones disponibles:

* Navegar a otra página
* Activar un marcador
* Volver atrás
* Quitar segmentaciones (reset filtros)
* Mostrar tooltip informativo

### Tipos más usados:

* Botones de navegación (experiencia tipo app)
* Botón de reinicio de filtros
* Botón activador de marcador
* Botón de ayuda o información

📌 Son esenciales para mejorar la experiencia de usuario y hacer el dashboard más interactivo.