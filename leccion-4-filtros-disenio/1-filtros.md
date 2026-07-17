
# 📊  Interacción y Experiencia en Dashboards

En esta lección aprendemos a **enriquecer dashboards** en Tableau mediante:

* Filtros.
* Mapas.
* Tooltips personalizados.
* Elementos visuales (imágenes, botones, textos, contenedores).

El objetivo es pasar de dashboards estáticos a **dashboards interactivos y más profesionales**.

---

# Filtros

Un filtro permite **limitar los datos que se muestran** en una visualización. ---

Los filtros permiten limitar la información que se muestra en una visualización para responder preguntas concretas o facilitar el análisis de los datos.

En Tableau existen diferentes tipos de filtros, cada uno con un propósito específico.

Sirve para:

* Analizar subconjuntos.
* Comparar segmentos.
* Mejorar rendimiento.
* Crear interacción en dashboards.

---

## Filtros básicos

Se aplican arrastrando un campo al estante de filtros.

Pueden ser:

* Por inclusión/exclusión.
* Por rango (ej: Sales > 5000).
* Por fecha (últimos 3 meses).

---

## Filtros interactivos

Permiten que el usuario cambie los datos desde el dashboard.

Para mostrarlos:

* Clic derecho en el filtro → **Show Filter**.

Tipos comunes:

* Lista múltiple.
* Dropdown.
* Slider.
* Filtro de fecha relativa.
* Wildcard (búsqueda por texto).

---

## Filtros Top N

Permiten mostrar:

* Top 10 productos.
* Top 5 regiones.
* Bottom 3 clientes.

Se configuran desde la pestaña **Top** en el cuadro del filtro.

**Buenas prácticas**

* No saturar con demasiados filtros.
* Usar filtros de contexto si hay varios.
* Nombrar claramente los filtros.
* Aplicar filtros globales solo si es necesario.


## Pasos para crear filtros

La forma más sencilla de crear un filtro es utilizando una dimensión.

## Paso 1. Crear una visualización

Por ejemplo:

* Columnas → Barrio
* Filas → Número de alojamientos

Obtendremos un gráfico de barras.

---

## Paso 2. Arrastrar un campo al estante Filtros

Selecciona el campo **Barrio** y arrástralo al estante **Filtros**.

Tableau mostrará una ventana donde podrás elegir los valores que deseas conservar.

Por ejemplo:

* Centro
* Salamanca
* Chamberí

Pulsa **Aceptar**.

La visualización mostrará únicamente esos barrios.

---

## Paso 3. Mostrar el filtro

El filtro ya existe, pero todavía no aparece para el usuario.

Haz clic derecho sobre el campo que está en el estante **Filtros** y selecciona:

**Mostrar filtro (Show Filter)**

Ahora aparecerá un panel lateral que permitirá modificar el filtro de forma interactiva.

---

# Tipos de filtros

Los filtros pueden mostrarse de diferentes formas según el tipo de dato.

## Lista única

Solo permite seleccionar un valor.

Ejemplo:

Provincia

○ Madrid

○ Barcelona

○ Valencia

---

## Lista múltiple

Permite seleccionar varios valores.

□ Madrid

☑ Barcelona

☑ Valencia

---

## Lista desplegable

Ocupa menos espacio y muestra las opciones al abrirla.

---

## Valores múltiples con búsqueda

Muy útil cuando existen cientos de categorías.

El usuario puede escribir parte del nombre.

Ejemplo:

```
Buscar...

Mad...
```

---

## Filtro de comodines (Wildcard)

Solo disponible para dimensiones de texto.

Permite buscar mediante texto.

Ejemplo:

```
*mad*
```

Mostrará:

Madrid

Madroño

Urbanización Madrid Norte

---

## Deslizador de rango

Utilizado para medidas o fechas.

Ejemplo:

Precio

```
100 € ─────────────── 500 €
```

---

## Fechas

Los filtros de fecha pueden mostrarse como:

* Año
* Trimestre
* Mes
* Semana
* Día
* Intervalo de fechas

---

# Filtros sobre dimensiones

Son los más utilizados.

Ejemplos:

* Barrio
* Tipo de habitación
* Anfitrión
* Provincia

Simplemente se arrastran al estante **Filtros**.

---

# Filtros sobre medidas

Las medidas permiten filtrar utilizando valores numéricos.

Ejemplo:

Precio

Podemos indicar:

* Mayor que
* Menor que
* Entre dos valores
* Suma
* Promedio
* Conteo

Ejemplo:

Mostrar únicamente viviendas con un precio superior a 100 €.

---

# Eliminar los valores NULL

Cuando una dimensión contiene valores nulos, Tableau mostrará la categoría **(Null)**.

Podemos eliminarla de varias formas.

### Método 1

Desmarcar **(Null)** desde el filtro.

### Método 2

Hacer clic derecho sobre **Null** en la visualización y seleccionar **Excluir**.

### Método 3

Crear un cálculo:

```tableau
NOT ISNULL([Barrio])
```

y filtrar por **True**.

---

# Aplicar un filtro a varias hojas

Cuando trabajamos con dashboards es habitual querer reutilizar un mismo filtro.

Haz clic sobre el menú del filtro y selecciona:

**Aplicar a hojas de trabajo**

Disponemos de tres opciones:

* Todas las hojas que usan esta fuente de datos.
* Hojas seleccionadas.
* Solo esta hoja.

Esta opción evita crear el mismo filtro varias veces.

---

# Orden de ejecución de los filtros

No todos los filtros se aplican al mismo tiempo.

De forma simplificada, Tableau sigue este orden:

1. Extract Filters
2. Data Source Filters
3. Context Filters
4. Dimension Filters
5. Measure Filters
6. Table Calculation Filters

Es importante conocer este orden porque afecta a los resultados obtenidos.

> **Consejo:** no es necesario memorizar el orden completo. Basta con entender que algunos filtros se ejecutan antes que otros y que un filtro de contexto puede cambiar el comportamiento de un filtro Top N.

---

# Crear un filtro Top N

Supongamos que queremos mostrar únicamente los **5 barrios con más alojamientos**.

## Paso 1

Crear una gráfica:

* Columnas → Barrio
* Filas → Número de registros

---

## Paso 2

Arrastrar **Barrio** al estante **Filtros**.

---

## Paso 3

Abrir la pestaña **Top**.

Seleccionar:

**Por campo**

Elegir:

* Top
* 5
* Por SUM(Number of Records)

Aceptar.

La visualización mostrará únicamente los cinco primeros barrios.

---

## Mostrar también el Bottom N

Podemos cambiar **Top** por **Bottom** para mostrar los cinco últimos.

---

# Usar una gráfica como filtro

No siempre es necesario colocar filtros laterales.

Una gráfica también puede actuar como filtro.

## Paso 1

Crear varias hojas.

Ejemplo:

* Barras por barrio.
* Mapa.
* Tabla.

---

## Paso 2

Crear un Dashboard.

---

## Paso 3

Seleccionar la gráfica principal.

En la esquina superior derecha pulsar:

**Usar como filtro (Use as Filter)**.

---

## Resultado

Al hacer clic sobre una barra:

* el mapa cambia,
* la tabla cambia,
* el resto de gráficos se actualizan automáticamente.

Es una de las funcionalidades más utilizadas en dashboards profesionales.

---

# Quitar un filtro

Para eliminar un filtro:

1. Selecciona el campo en el estante **Filtros**.
2. Pulsa **Suprimir** o arrástralo fuera del estante.

Si el filtro estaba visible en el dashboard, desaparecerá automáticamente.

---

## Buenas prácticas

* Usa dimensiones para filtrar categorías y medidas para filtrar valores numéricos.
* Muestra solo los filtros que realmente necesite el usuario.
* Evita llenar el dashboard con demasiados filtros.
* Siempre revisa si existen valores **NULL** antes de presentar una visualización.
* Cuando varias hojas deban responder al mismo filtro, utiliza **Aplicar a hojas de trabajo**.
* Siempre que sea posible, utiliza una **gráfica como filtro** para crear dashboards más intuitivos y reducir el número de controles visibles.

