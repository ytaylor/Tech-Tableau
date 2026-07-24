
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

## Marcadores (Bookmarks)

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

### Pasos para crear un marcador:
Ver/Marcadores → Panel de Marcadores → Crear nuevo marcador → Configurar opciones.
Botones - Navegadores - Navegadores de Marcadores

---

## Botones Interactivos

Los **botones** permiten ejecutar acciones con un clic, acciones disponibles:

* Navegar a otra página
* Activar un marcador
* Volver atrás
* Quitar segmentaciones (reset filtros)
* Mostrar tooltip informativo

### Pasos para crear un botón:
- Insertar → Botón → Configurar acción (tipo de acción, destino, estilo).
- Se pueden configuraar el boton vaya a algín sitio específico, o que active un marcador, o que haga reset de filtros.
- **Boton de borrar segmentaciones:** sirve para borrar todos los filtros aplicados en la página, dejando la visualización en su estado original. Insertar → Botón → Borrar segmentaciones → Configurar acción. Solo funciona si hay segmentaciones en la página, no aplica a los filtros de nivel de página o de nivel de informe.
- **Boton de informacion:** sirve para mostrar información adicional sobre la visualización, el informe o la empresa. Insertar → Botón → Información → Configurar acción. Se puede configurar para que muestre un tooltip con información adicional, o que abra una página de información.