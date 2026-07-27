
# 📊 Personalización de Dashboards en Power BI

En esta lección se aprende a enriquecer informes mediante visualizaciones analíticas y herramientas avanzadas de navegación .


## Organización y Diseño del Dashboard

Se trabajan buenas prácticas de diseño :

* Jerarquía visual clara (título → KPIs → gráficos → filtros).
* Distribución ordenada y alineada.
* Enfoque en la toma de decisiones.
* Uso coherente de colores y espacios.

El objetivo es crear dashboards claros, estructurados y profesionales.

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

## Parámetros, Grupos y Columnas Condicionales 

Estas herramientas permiten hacer dashboards más dinámicos y estructurados.
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
Ver/seleccion - seleccionar lo que quiero que se vea en cada momento. 
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