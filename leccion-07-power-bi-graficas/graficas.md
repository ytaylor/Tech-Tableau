
# Gráficas en Power BI
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
  
  - Se puede activar la etiqueta de datos para mostrar valores exactos.
  - Hay diferentes tipos de graficas:
    - **Grafico de barras apiladas**
    - **Grafico de barras agrupadas**: Permite comparar varias categorías dentro de un mismo eje.
    - **Grafico de columnas agregadas**: Permite ver la suma de varias categorías en un mismo eje.
    - **Grafico de 100% apiladas**: Permite ver la proporción de cada categoría respecto al total.
  
* 📈 **Líneas** → Tendencias en el tiempo.
  * Explicar el eje secundario y cómo se puede usar para comparar dos métricas con escalas diferentes.
  * Tambien puedo añadir leyendas
  * Se puede añadir año, trimestre, mes, semana, día, hora, minuto, segundo como eje X.
* **Áreas**: Permite ver la evolución de una métrica en el tiempo, mostrando la magnitud del cambio.
  * Grafico de areas apiladas. 
* 🥧 **Pie (Quesito)** → Parte de un total.
* 🗺 **Mapas** → Datos geográficos.
  * Activar la opción en power Bi en Opiciones - Seguridad - Habilitar visualizaciones de mapas.
  * Cambiar el tipo de datos para poder usarlo en el mapa (ej. ciudad, país, CP, coordenadas).
  * Tamaño de la burbuja según métrica.
* 🎯 **KPI** → Métricas clave.
  * **Tarjetas de varias filas:** permiten mostrar varias métricas en un mismo visual.
* **Embudo**: Ordena los datos.
* Esquema jerarquico: Permite ver la relación entre diferentes niveles de datos.
* **Histogramas:** Permite ver la distribución de los datos en intervalos.
  * Crear nuevo grupo de datos para poder crear el histograma.
  * Crear por el tamaño de discretizaciones. 
  * Arrastrar ese grupo al eje X y al eje Y
* **Scatter:** Permite ver la relación entre dos métricas.
  * Elegir el grafico de dispersión y arrastrar las métricas al eje X y al eje Y. (por ejemplo el total vendido y el valor de tasacion de las casas)
  * Ejemplo de scatter:
    * Valores: Comunidad Autonoma, Eje X: Primedio por valor cuadrado, Eje Y: Valor por tasación, Leyenda: Comunidad Autonoma, Tamaño: Total vendido.


También se pueden añadir gráficos adicionales desde el marketplace.

Se pude maquetar desde el principio como quiero que sea la estrutura de mi dashboard, para que luego solo tenga que arrastrar los campos.

Se pueden poner los graficos en modo enfocado, para que se vean más grandes y con más detalle.

---

## Creación de gráficos 

Ejemplo práctico (ventas por estado):

1. Seleccionar gráfico (ej. columnas).
2. Arrastrar dimensión al eje X.
3. Arrastrar métrica al eje Y.
4. Ajustar agregación (suma, promedio, etc.).
5. Aplicar filtros si es necesario.
6. Formatear colores, ejes, etiquetas.

💡 Se puede cambiar el tipo de gráfico sin perder los campos arrastrados.


## Mapas en Power BI 

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

## Filtros y Segmentos (Slicers) 

### Segmentos (Slicers)

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

### Filtros

Más técnicos y precisos.

Tipos:

* Nivel visual
* Nivel página
* Nivel informe

- No son visibles por defecto, pero se pueden mostrar en el panel lateral.
- Importancia de la jerarquía: los filtros de nivel visual tienen prioridad sobre los de nivel página, y estos sobre los de nivel informe.


Ventajas:

* Mayor control.
* Permiten condiciones complejas.
* No visibles por defecto.

---

## Uso compartido 

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
## Actualización de datos ya cargados 
Si quiero actualizar los datos cargados, le doy a Tranformar Datos y en Configuracion de Origen de Datos puedo actualizar la conexión a la fuente de datos.