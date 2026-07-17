# Mapas

Los mapas permiten representar **datos geográficos**.

Se usan para:

* Analizar distribución.
* Detectar patrones por zona.
* Visualizar concentración.

**¿Qué reconoce Tableau como geográfico?**

* País.
* Provincia.
* Ciudad.
* Código postal.
* Latitud y Longitud.

Si no lo reconoce:

* Asignar rol geográfico.
* Añadir coordenadas.
* Corregir nombres.

**Cómo crear un mapa básico**

1. Arrastrar campo geográfico.
2. Tableau genera el mapa automáticamente.
3. Añadir medida a:

   * Color (intensidad).
   * Tamaño (magnitud).
   * Etiqueta (valor visible).

**Personalización de mapas**

* Cambiar paleta de colores.
* Ajustar tamaño de puntos.
* Activar nombres y límites en capas del mapa.
* Elegir fondo (estándar, satélite, claro).

Buenas prácticas
* Usar mapa solo si el factor geográfico es relevante.
* No saturar con demasiados puntos.
* Añadir filtros para mejorar lectura.
* Asegurar correcta geolocalización.


## 🧩 Viz in Tooltip (Gráfica dentro del tooltip)

Permite insertar una visualización secundaria dentro del tooltip.
Pasos:

1. Crear visualización secundaria.
2. Ir al tooltip de la hoja principal.
3. Insertar hoja secundaria con:
   `Insert > Sheets`.

Ejemplo:

* Mapa por región.
* Tooltip muestra ventas por producto.

Buenas prácticas

* Que la vista secundaria sea clara y pequeña.
* Evitar scroll horizontal.
* No saturar con demasiado texto.
* Usar solo si aporta valor real.

Te propongo un capítulo muy práctico, igual que los anteriores del manual. Está pensado para que el alumno aprenda primero los conceptos y luego cree diferentes tipos de mapas.

---

# Capítulo 5. Mapas en Tableau

Los mapas permiten representar datos geográficos de forma visual para identificar patrones, comparar ubicaciones y detectar zonas con mayor o menor actividad.

Tableau incorpora un sistema de geocodificación que reconoce países, ciudades, provincias, códigos postales y coordenadas geográficas.

> **Importante**
>
> No todos los campos de texto representan una ubicación válida. Si Tableau no reconoce una ubicación, será necesario asignar un rol geográfico o utilizar coordenadas (Latitud y Longitud).

---

# 5.1 Roles geográficos

Para que Tableau pueda crear un mapa, necesita saber qué representa cada campo.

Los roles geográficos más utilizados son:

* País
* Estado o Provincia
* Ciudad
* Código Postal
* Latitud
* Longitud

Para cambiar un rol geográfico:

1. Haz clic derecho sobre el campo.
2. Selecciona **Geographic Role**.
3. Elige el tipo de ubicación correspondiente.

> **Consejo:** Si Tableau no reconoce correctamente una ubicación, revisa siempre el rol geográfico antes de continuar.

---

# 5.2 Crear un mapa automáticamente

Si Tableau reconoce el campo geográfico, crear el mapa es muy sencillo.

### Paso 1

Haz doble clic sobre un campo geográfico.

Por ejemplo:

* Country
* State
* City

Tableau generará automáticamente un mapa.

### Paso 2

Arrastra una medida como:

* Number of Records
* Price
* Reviews

sobre **Color** o **Size**.

Ahora el mapa mostrará información además de la ubicación.

---

# 5.3 Crear un mapa con Latitud y Longitud (Airbnb)

En el dataset de Airbnb se incluyen las columnas:

* Latitude
* Longitude

Estas columnas contienen la posición exacta de cada alojamiento.

Esta es la forma más precisa de crear un mapa.

### Paso 1

Arrastra **Longitude** al estante de **Columnas**.

### Paso 2

Arrastra **Latitude** al estante de **Filas**.

Tableau generará automáticamente un mapa con todos los alojamientos.

### Paso 3

En la tarjeta **Marcas**, cambia el tipo de marca a **Circle**.

### Paso 4

Arrastra **Neighbourhood Group** a **Color**.

Cada distrito aparecerá con un color diferente.

### Paso 5

Arrastra **Neighbourhood** a **Detalle**.

Cada punto representará un alojamiento ubicado en su barrio correspondiente.

### Paso 6

Arrastra **Price** a **Tamaño** para representar el precio mediante el tamaño de los puntos.

### Paso 7

Arrastra **Room Type** a **Filtro** para poder visualizar únicamente determinados tipos de alojamiento.

---

## Resultado

Obtendrás un mapa donde:

* Cada punto representa un alojamiento.
* El color indica el distrito.
* El tamaño representa el precio.
* Los filtros permiten analizar diferentes tipos de viviendas.

---

# Personalizar el mapa

Desde el menú:

**Mapa → Capas del mapa**

podrás modificar:

* Fondo del mapa
* Calles
* Nombres de ciudades
* Edificios
* Terreno
* Límites administrativos

Esto permite adaptar el mapa según el tipo de análisis.

---

# Añadir información al Tooltip

Para enriquecer el mapa:

1. Arrastra los campos a **Tooltip**.

Por ejemplo:

* Nombre del alojamiento
* Precio
* Tipo de habitación
* Número de valoraciones
* Barrio

Al pasar el ratón sobre un punto aparecerá toda esta información.

---

# Utilizar filtros en el mapa

Los mapas también pueden filtrarse igual que cualquier otra visualización.

Por ejemplo:

* Tipo de habitación.
* Barrio.
* Distrito.
* Precio.
* Número mínimo de noches.

Para mostrar el filtro:

1. Arrastra el campo a **Filtros**.
2. Haz clic derecho sobre él.
3. Selecciona **Mostrar filtro**.

---

# ¿Por qué Tableau coloca todos los puntos en Madrid?

Es uno de los errores más frecuentes al trabajar con mapas.

Si utilizamos únicamente el campo **Neighbourhood**, Tableau intenta localizar ese nombre como si fuera una ciudad.

Por ejemplo:

| Barrio   | Tableau puede interpretar     |
| -------- | ----------------------------- |
| Sol      | Otra localidad llamada Sol    |
| Justicia | Otro municipio                |
| Palacio  | Otra ubicación con ese nombre |

Como consecuencia, muchos barrios aparecen mal ubicados o todos se sitúan en Madrid.

## Solución

La forma más fiable es utilizar las columnas **Latitude** y **Longitude**, ya que contienen la posición exacta de cada alojamiento y no dependen de que Tableau interprete correctamente el nombre del barrio.

---

# Paso a paso: Crear un mapa de Airbnb en Madrid

1. Arrastra **Longitude** a Columnas.
2. Arrastra **Latitude** a Filas.
3. Cambia el tipo de marca a **Circle**.
4. Arrastra **Neighbourhood Group** a **Color**.
5. Arrastra **Price** a **Size**.
6. Arrastra **Room Type** a **Filtro**.
7. Arrastra **Name** y **Reviews** a **Tooltip**.

### Preguntas para analizar

* ¿Qué distritos concentran más alojamientos?
* ¿Dónde se encuentran los alojamientos más caros?
* ¿Qué tipo de habitación es más frecuente?
* ¿Existen zonas con mayor concentración de viviendas turísticas?