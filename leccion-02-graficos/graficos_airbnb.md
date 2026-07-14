

## 1. ¿Qué distritos tienen más alojamientos?
### 📊 Gráfico: **Barras**

**Por qué**

* Ideal para comparar categorías.
* Muy fácil de leer.

**Campos**

* `neighbourhood_group` → Columnas
* `COUNT(id)` → Filas


---

## 2. ¿Cómo varía el precio según el distrito?

### 📊 Gráfico: **Barras (precio medio)**

**Por qué**

* Introduce agregaciones (`AVG`).
* Comparación clara entre zonas.

**Campos**

* `neighbourhood_group` → Columnas
* `AVG(price)` → Filas
---

## 3. ¿Qué tipos de alojamiento hay?

### 📊 Gráfico: **Barras o pastel**

**Por qué**

* Variable categórica con pocas opciones.
* Sirve para hablar de proporciones.

**Campos**

* `room_type` → Columnas / Color
* `COUNT(id)` → Filas

---

## 4. ¿Cuál es el tipo de alojamiento más caro?

### 📊 Gráfico: **Barras**

**Por qué**

* Comparación directa entre categorías.
* Refuerza uso de `AVG()`.

**Campos**

* `room_type` → Columnas
* `AVG(price)` → Filas

---

## 5. ¿Existe relación entre precio y número de reviews?


### 📊 Gráfico: **Dispersión**

**Por qué**

* Sirve para ver relaciones entre variables.
* Introduce gráficos más “analíticos”.

**Campos**

* `price` → Columnas
* `number_of_reviews` → Filas

💡 Variante:

* Color → `room_type`

> “Relación entre dos números → dispersión.”

---

## 6. ¿Qué barrios son más caros

### 📊 Gráfico: **Barras (Top N)**

**Por qué**

* Introduce filtros y ordenación.
* Muy realista para dashboards.

**Campos**

* `neighbourhood` → Filas
* `AVG(price)` → Columnas

➕ Filtro:

* Top 10 barrios por precio medio.

---

## 7. ¿Cuántos alojamientos hay disponibles todo el año?

### 📊 Gráfico: **Big Number**

**Por qué**

* KPI claro.
* Introduce visualizaciones resumen.

**Campos**

* `COUNT(id)`
* Filtro: `availability_365 > 300`

Ejemplo:

> “Alojamientos disponibles casi todo el año”

