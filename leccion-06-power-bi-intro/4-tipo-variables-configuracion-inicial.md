# Configuración Regional, Fechas y Variables

### 📂 Importación de Datos y Origen Regional

Cuando importamos un archivo CSV, Excel o TXT en Power BI, es esencial configurar correctamente el **origen de archivo**.

#### ¿Qué es el origen regional?

El origen regional determina:

* **El formato de fechas** (dd/mm/yyyy vs mm/dd/yyyy).
* **El separador decimal** (coma vs punto).
* **El delimitador de columnas** (coma, punto y coma, tabulador...).

#### ⚙️ ¿Dónde se configura?

Al importar un archivo, Power BI te permite:

1. Seleccionar el **archivo origen**.
2. En la ventana previa ("Preview"), hacer clic en **Transformar datos**.
3. Luego en la pestaña **Archivo** → **Configuración de origen de archivo**:
   * Elige la codificación correcta (por defecto suele ser UTF-8).
   * Ajusta el **delimitador** (ej. `;`, `,`, `tab`).
   * Establece el **origen regional** según cómo se ha guardado el archivo.

💡 _Ejemplo: Si estás usando un archivo generado en España, el origen regional correcto sería “Español (España)”._

***

### Delimitadores: separando columnas

Un **delimitador** es el carácter que separa las columnas en archivos de texto (CSV o TXT).

| Tipo de archivo | Delimitador común |
| --------------- | ----------------- |
| `.csv` España   | `;`               |
| `.csv` EE.UU.   | `,`               |
| `.tsv`          | `tabulador`       |

⚠️ Si el delimitador no se selecciona correctamente, Power BI mostrará todos los datos en una sola columna.

***

### Tipos de datos en Power BI

Después de importar, cada columna tiene un **tipo de dato** asignado automáticamente. Es crucial verificar que se haya asignado correctamente.

| Tipo de dato      | Ícono | Ejemplo            |
| ----------------- | ----- | ------------------ |
| Texto (cadena)    | `ABC` | `"Barcelona"`      |
| Número entero     | `123` | `42`               |
| Número decimal    | `1.2` | `3,1416`           |
| Fecha             | `📅`  | `13/06/2025`       |
| Fecha y hora      | `🕒`  | `13/06/2025 14:30` |
| Booleano (lógico) | `✔/✘` | `TRUE / FALSE`     |
| Moneda            | `€`   | `€ 50,00`          |

#### Cómo cambiar el tipo de dato

1. En el **Editor de Power Query**, selecciona la columna.
2. Haz clic en el ícono del tipo de dato (a la izquierda del nombre de columna).
3. Elige el tipo correcto del desplegable.

💡 _Es buena práctica revisar todas las columnas justo después de importar los datos._

***

### Errores comunes al importar datos

* **Fechas mal interpretadas**: por una mala configuración regional.
* **Números como texto**: impide hacer cálculos.
* **Campos vacíos o nulos**: pueden generar errores en visualizaciones o medidas DAX.

***

### 📊 Jerarquía de Fechas en Power BI

La **jerarquía de fechas** en Power BI es una estructura automática que permite analizar datos a diferentes niveles de tiempo: **Año > Trimestre > Mes > Día**. Se crea automáticamente cuando arrastras un campo de tipo `date` a un gráfico.

* Facilita el **análisis temporal** sin crear columnas manualmente.
* Permite **navegar fácilmente entre niveles** de detalle temporal.
* Mejora la **interactividad** con visualizaciones como gráficos de líneas o columnas.

***

#### 🛠️ Cómo se usa paso a paso

**1. Tener una columna tipo fecha**

* Asegúrate de que la columna esté en formato `date`.
* Ejemplo: `FechaPedido`, `FechaVenta`, etc.

**2. Arrastrar el campo de fecha a una visualización**

* Power BI genera automáticamente una jerarquía:**Año > Trimestre > Mes > Día**

**3. Explorar la jerarquía**

* Haz clic en los iconos de **expandir** (`+`) o usa el botón derecho para cambiar entre:
  * Expandir toda la jerarquía
  * Ver sólo un nivel a la vez

**4. Personalizar la jerarquía**

* Puedes **modificar el orden** o **eliminar niveles**.
* También puedes crear **una jerarquía personalizada** arrastrando manualmente campos calculados como `Año`, `MesNombre`, etc.

***

#### ✍️ Ejemplo

Tienes una tabla de ventas con la columna `FechaVenta`. Arrastras esa columna a un gráfico de líneas. Power BI automáticamente crea una jerarquía:

```
FechaVenta
🌐│
🕊│— Año
🕊│— Trimestre
🕊│— Mes
🕊└— Día
```

Ahora puedes ver cómo evolucionan las ventas **a lo largo de los años, meses o días**, sin hacer cálculos adicionales.

#### 🔧 ¿Y si no se crea automáticamente?

* A veces Power BI **no detecta bien la columna** como fecha.
* Solución: En el panel de campos, haz clic en el campo y cambia el tipo de datos a **Date**.

***

#### 💡 Buenas prácticas

* Usa jerarquías si necesitas **resumen + detalle** temporal.
* Para mayor control, crea una **tabla de fechas personalizada** (`Calendar table`).
* Usa `DATEADD`, `SAMEPERIODLASTYEAR`, etc. para cálculos más avanzados.
* Siempre revisa el **origen regional y delimitador** al importar.
* Verifica que cada columna tenga el **tipo de dato adecuado**.
* Usa la vista previa del Editor de Power Query para inspeccionar tus datos.
* Documenta cambios importantes aplicados durante la transformación de datos.
