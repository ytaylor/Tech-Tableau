## Graficos de Lineas

El **gráfico de líneas** se utiliza para mostrar la **evolución de una medida a lo largo del tiempo** o siguiendo un orden lógico.

1. **Abre una hoja nueva.**

2. **Arrastra una dimensión** al estante **Columnas**.

   * Normalmente una **fecha** (`Date`) o una variable ordenada.

3. **Arrastra una medida** al estante **Filas**.

   * Ejemplo: `AVG(Price)` o `SUM(Sales)`.

4. Tableau suele crear automáticamente un **gráfico de líneas**.

5. Si no lo hace:

   * Haz clic en **Mostrarme (Show Me)**.
   * Selecciona el icono **Gráfico de líneas**.

---

## Ejemplo con Airbnb

Quieres ver cómo evoluciona el **precio medio** según la fecha.

* **Columnas** → `Last Review` (Mes o Año).
* **Filas** → `AVG(Price)`.

Obtendrás una línea que muestra la evolución del precio medio a lo largo del tiempo.

---

## Si quieres varias líneas

Añade una dimensión a **Color** en la tarjeta **Marcas**.

Por ejemplo:

* **Columnas** → `Last Review`
* **Filas** → `AVG(Price)`
* **Color** → `Room Type`

Obtendrás una línea para cada tipo de habitación.

---

## Ejes Dobles
1. **Arrastra la dimensión** a **Columnas**.

   * Ejemplo: `Neighbourhood Group`.

2. **Arrastra la primera medida** a **Filas**.

   * Ejemplo: `COUNT(Number of Records)`.

3. **Arrastra la segunda medida** también a **Filas**, a la derecha de la primera.

   * Ejemplo: `AVG(Price)`.

4. **Haz clic derecho sobre el segundo eje** (`AVG(Price)`).

5. Selecciona **Eje doble (Dual Axis)**.

6. En la tarjeta **Marcas**, configura cada medida:

   * Primera medida → **Barra**.
   * Segunda medida → **Línea**.

7. *(Opcional)* Haz clic derecho sobre un eje y selecciona **Sincronizar ejes (Synchronize Axis)** si quieres que ambos utilicen la misma escala.

8. *(Opcional)* Cambia los colores de cada medida para diferenciarlas mejor.

--- 
## Histogramas
1. Abre una **hoja nueva**.
2. Selecciona el **campo numérico**.
   * Ejemplo: `Price`.
3. Haz clic en **Mostrarme (Show Me)**.
4. Selecciona el icono **Histograma**.
5. Tableau crea automáticamente:
   * Los **intervalos (Bins)**.
   * El **Número de registros (Count)**.
   * El **histograma**.


### Si quieres personalizar el histograma

* Cambiar el **tamaño de los intervalos (bins)**.
* Cambiar colores.
* Añadir etiquetas.
* Aplicar filtros.

💡 **Regla para recordar:** un **histograma** muestra la **distribución de una variable numérica**, agrupando los datos en intervalos (bins). En Tableau 2026.2 basta con seleccionar la medida y elegir **Mostrarme → Histograma**.


## Pastel 

### Opción 1 (la más fácil)

1. Selecciona una **dimensión** (por ejemplo, `Room Type`) y una **medida** (por ejemplo, `COUNT(Number of Records)` o `Price`).
2. Haz clic en **Mostrarme (Show Me)**.
3. Selecciona **Gráfico de pastel**.


---

### Opción 2 (manual)
En la tarjeta **Marcas**:
1. Cambia el tipo de marca de **Automático** a **Pastel**.
2. Cuando el tipo sea **Pastel**, deberían aparecer opciones como:

   * **Color**
   * **Tamaño**
   * **Etiqueta**
   * **Detalle**
   * **Información emergente (Tooltip)**

--- 

## Donut
El **gráfico de donut (anillo)** **no existe como tipo de gráfico nativo en Tableau**. Se crea utilizando un **gráfico de pastel + un eje doble (Dual Axis)** para colocar un círculo blanco en el centro.

### Paso 1. Crea un gráfico de pastel
1. Abre una hoja nueva.
2. Cambia el tipo de marca a **Pastel**.
3. Arrastra la **dimensión** a **Color**.

   * Ejemplo: `Room Type`.
4. Arrastra la **medida** a **Ángulo**.

   * Ejemplo: `COUNT(Number of Records)`.

### Paso 2. Crear un eje doble

5. Haz doble clic en una zona vacía de **Columnas** y escribe:

```text
MIN(1)
```

6. Repite la operación para tener dos veces **MIN(1)** en **Columnas**.

7. Haz clic derecho sobre el segundo **MIN(1)** y selecciona **Eje doble (Dual Axis)**.

### Paso 3. Configurar las marcas

En la tarjeta **Marcas** aparecerán tres pestañas:

* **Todo**
* **MIN(1)**
* **MIN(1)**

#### Primer MIN(1)

* Tipo de marca → **Pastel**.
* Configura el gráfico como antes (Color y Ángulo).

#### Segundo MIN(1)

* Tipo de marca → **Círculo**.
* Color → **Blanco**.
* Reduce ligeramente el tamaño del círculo para que quede un agujero en el centro.




## Mostrar el porcentaje del total

1. Crea el gráfico de pastel.
2. Arrastra la medida (por ejemplo, **COUNT(Number of Records)**) a **Etiqueta (Label)**.
3. En la tarjeta **Marcas**, haz clic sobre la píldora de la medida que está en **Etiqueta**.
4. Selecciona:

   * **Cálculo rápido de tabla (Quick Table Calculation)**.
   * **Porcentaje del total (Percent of Total)**.
5. Si es necesario, cambia el formato:

   * Haz clic derecho sobre la medida.
   * **Formato** → **Números** → **Porcentaje**.


--- 
## Personalizacion 
- Uso del color: seleccionar color con el puntero, colores aportan información, eelegir colores diferentes segun lo que representa cada variable_ https://coolors.co/ 
- Anotaciones
- Formas Personalizadas
- Quitar elementos innecesarios
- Uso de lA IA: recraf IA: crear una paleta de colores profesionales para Airbnb
- Destacar categorias_ 
     - Usa el mismo color para cada categoria
     - Usar un color para darle importancia a esa categoria
     Usar Highlight (la más sencilla)
        1. Crea tu gráfico.
        2. Arrastra la dimensión (por ejemplo, Neighbourhood Group) a Color.
        3. Haz clic derecho sobre esa dimensión en la tarjeta Marcas.
        4. Selecciona Mostrar resaltador (Show Highlighter).
        5. Aparecerá una caja de búsqueda a la derecha.
        6. Cuando escribas por ejemplo Madrid, Tableau: Resaltará Madrid con su color. Atenuará el resto de categorías.

--- 
## Crear agrupaciones:
Si estás utilizando el **dataset de Airbnb Madrid**, un ejemplo mucho más realista es agrupar los **distritos** o **barrios** por zonas de la ciudad.

## Ejemplo: Agrupar distritos de Madrid

Supongamos que el campo es **Neighbourhood Group** o **Distrito** y contiene:

* Centro
* Salamanca
* Chamberí
* Chamartín
* Retiro
* Arganzuela
* Carabanchel
* Latina
* Usera
* Villaverde
* Puente de Vallecas
* Hortaleza
* Moncloa-Aravaca
* Tetuán
* Fuencarral-El Pardo
* ...

Puedes crear grupos como estos:

| Grupo      | Distritos                                                          |
| ---------- | ------------------------------------------------------------------ |
| **Centro** | Centro, Salamanca, Chamberí, Retiro                                |
| **Norte**  | Chamartín, Tetuán, Fuencarral-El Pardo, Hortaleza, Moncloa-Aravaca |
| **Sur**    | Usera, Villaverde, Carabanchel, Puente de Vallecas, Latina         |

---

## Paso a paso en Tableau

1. Haz clic derecho sobre **Neighbourhood Group** (o **Distrito**).
2. Selecciona **Crear → Grupo**.
3. Selecciona:

   * Centro
   * Salamanca
   * Chamberí
   * Retiro
4. Haz clic en **Agrupar**.
5. Cambia el nombre a **Centro**.
6. Repite el proceso con los distritos del **Norte** y del **Sur**.
7. Pulsa **Aceptar**.

Se creará el campo:

```text
Neighbourhood Group (group)
```

---

## ¿Cómo utilizar el grupo?

Por ejemplo, para comparar el precio medio por zona:

* **Columnas** → `Neighbourhood Group (group)`
* **Filas** → `AVG(Price)`

Obtendrás un gráfico de barras con:

```
Centro   ████████████ 220 €
Norte    ████████     150 €
Sur      █████        95 €
```

---

## Otro ejemplo: Agrupar por nivel turístico

En lugar de agrupar por ubicación geográfica, puedes hacerlo por interés turístico.

| Grupo              | Distritos                                 |
| ------------------ | ----------------------------------------- |
| **Muy turísticos** | Centro, Salamanca                         |
| **Residenciales**  | Chamartín, Hortaleza, Fuencarral-El Pardo |
| **Periféricos**    | Villaverde, Usera, Carabanchel, Latina    |

Después puedes analizar:

* Precio medio.
* Número de alojamientos.
* Número de reseñas.
* Disponibilidad.



