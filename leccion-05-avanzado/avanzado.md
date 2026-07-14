
# 📊  Lección 05: Dashboards Avanzados en Tableau

---

## 🚀 1. Introducción: Dashboards más interactivos y estratégicos

En este bloque aprendemos a llevar los dashboards a un nivel más profesional, incorporando:

* Interactividad
* Narrativa de datos
* Control dinámico
* Métricas estratégicas

El objetivo no es solo visualizar datos, sino convertir el dashboard en una herramienta de toma de decisiones .


## 2. Más personalizaciones

###  Crear Paleta Personalizada 
1. Cierra Tableau completamente
2. Navega a la carpeta de preferencias:
   - Windows: C:\Users\[TuUsuario]\Documents\My Tableau Repository\Preferences.tps
   - Mac: ~/Documents/My Tableau Repository/Preferences.tps
3. Edita el archivo Preferences.tps con un editor de texto (Notepad++, Sublime, VS Code)
4. Añade tu paleta personalizada dentro de las etiquetas <preferences>:


###  IA: Pedirle a la IA que me diga sugerencias para mejorar el diseño de mi dashboard

1. Elige un dashboard que hayas creado
2. Describe el contexto y objetivo del dashboard
3. Pídele a la IA que te sugiera mejoras de diseño, interactividad o narrativa
4. Implementa las sugerencias y compara resultados. 


## 
---

# 🎯 3. Acciones en Dashboards

Las **acciones** permiten que el usuario interactúe con las visualizaciones.

### Tipos de acciones

1. **Acciones de filtro** → Una selección afecta a otras vistas
2. **Acciones de navegación** → Ir a otra hoja, dashboard o URL
3. **Acciones de resaltado (Highlight)** → Resaltar datos relacionados

📌 Se configuran desde:
`Dashboard → Acciones → Agregar acción`

### Buenas prácticas

* Filtro → Para drill-down dinámico
* Resaltado → Para comparar sin ocultar datos
* Navegación → Para dividir dashboards complejos
* Siempre explicar cómo interactuar 

---

# 🗂 4. Grupos de Datos

Un **grupo** permite agrupar manualmente valores de una dimensión.

Ejemplo:

* Varias ciudades → “Región Norte”
* Marcas pequeñas → “Otras marcas”

### Cuándo usar grupos

* Simplificar visualizaciones
* Reducir categorías
* Crear agrupaciones personalizadas

### Grupo vs Conjunto

| Grupo                | Conjunto                |
| -------------------- | ----------------------- |
| Manual               | Manual o condicional    |
| Crea nueva dimensión | Booleano (dentro/fuera) |

Los grupos ayudan a hacer dashboards más claros y comprensibles .

---

# 🎛 5. Parámetros

Un **parámetro** es un valor dinámico independiente del dataset.

Permite:

* Cambiar métricas
* Crear análisis What-If
* Controlar cálculos
* Intercambiar dimensiones

⚠️ Importante:
Un parámetro **no hace nada por sí solo**, debe usarse en:

* Campos calculados
* Filtros
* Acciones

Ejemplo:

```tableau
CASE [Seleccionar métrica]
 WHEN "Ventas" THEN [Ventas]
 WHEN "Beneficio" THEN [Beneficio]
END
```

Los parámetros mejoran la experiencia interactiva del usuario .

---

# 🧮 6. Campos Calculados

Permiten crear nuevas métricas o dimensiones a partir de los datos existentes.

## Tipos

1. **Cálculos básicos** (fila o agregados)
2. **LOD (Level of Detail)** → INCLUDE, EXCLUDE, FIXED
3. **Cálculos de tabla** → Solo a nivel de visualización

Se crean desde:
`Panel de datos → Crear campo calculado`

Los campos calculados amplían enormemente el poder analítico de Tableau .

---

# 🔢 6. Funciones en Tableau

## 🔹 Funciones Numéricas

* ABS
* ROUND
* FLOOR
* CEILING
* SQRT
* MAX / MIN

**Ejemplos**:
- 📌 Problema: Hay precios negativos por error: `ABS([Price])`
- 📌 Problema: Quiero redondear ventas a miles: `ROUND([Sales], -3)`
- 📌 Problema: Clasificar noches en bloques enteros: `FLOOR([Noches])`,  `CEILING([Noches])`


## 🔹 Funciones de Cadena

* SPLIT
* CONTAINS
* REPLACE
* LEN
* LOWER / UPPER

**Ejemplos**:
- 📌 Problema: Extraer país de “Ciudad, País”: `SPLIT([Ciudad, País], ",", 2)`
- 📌 Problema: Detectar si el nombre contiene “Hotel”: `CONTAINS([Nombre], "Hotel")`
- 📌 Problema: Reemplazar “N/A” por “Desconocido”: `REPLACE([Campo], "N/A", "Desconocido")`
- 📌 Problema: Contar caracteres de una reseña: `LEN([Reseña])`


## 🔹 Funciones Lógicas

* IF / ELSEIF / ELSE
* AND
* OR
* NOT
* IN

**Ejemplos**:
- 📌 Problema: Clasificar precios:
```tableau
IF [Precio] > 100 THEN "Caro"
ELSEIF [Precio] > 50 THEN "Medio"   
ELSE "Barato"
END
```

- 📌 Problema: Detectar si el país es España o Portugal: `[País] IN ("España", "Portugal")`
- 📌 Problema: Detectar si el país no es España ni Portugal: `NOT [País] IN ("España", "Portugal")`

Permiten crear clasificaciones como:

* “Caro / Medio / Barato”
* “Revisar datos”
* “Cumple objetivo”

## 🔹 Funciones de Agregación

* SUM
* AVG
* MIN
* MAX
* COUNT
* COUNTD
* STDEV

⚠️ Regla clave:
No se puede mezclar un valor agregado con uno no agregado en el mismo cálculo.

## 📅 Funciones de Fecha

Permiten:

* Agrupar por mes, trimestre, año
* Calcular diferencias de tiempo
* Detectar estacionalidad

**Ejemplo**:
- 📌 Problema: Agrupar por trimestre: `DATETRUNC('quarter', [Fecha])`
- 📌 Problema: Calcular antigüedad en días: `DATEDIFF('day', [Fecha de registro], TODAY())`
- 📌 Problema: Detectar si la fecha es fin de semana: `DATENAME('weekday', [Fecha]) IN ("Saturday", "Sunday")`
- 📌 Agrupar reservas por año: `DATETRUNC('year', [Fecha])`

## Funciones Geográficas
- 👉 Crear puntos en un mapa: `MAKEPOINT([Latitud], [Longitud])`
- 👉 Calcular distancia entre dos puntos: `DISTANCE([Punto1], [Punto2])`
- 👉 Crear líneas entre puntos: `MAKELINE([Punto1], [Punto2])`
- 👉 Crear un buffer alrededor de un punto: `BUFFER([Punto], [Distancia])`

---

# 📖 7. Historias en Tableau

Una **historia** es una secuencia de dashboards u hojas que construyen una narrativa.

Está formada por **puntos de historia**.

### Beneficios

* Guía al usuario
* Añade contexto
* Facilita toma de decisiones
* Mejora engagement

Se crea desde:
`Historia → Nueva historia`

Ideal para presentaciones ejecutivas 

---

# 📈 8. KPIs y Métricas

Antes de diseñar un dashboard hay que preguntarse:

👉 ¿Para quién es?
👉 ¿Qué decisiones debe apoyar?

## 🔹 KPI (Key Performance Indicator)

Indicador estratégico ligado a objetivos y plazos.

Ejemplo:

* “Aumentar ventas un 10% en el próximo trimestre”

## 🔹 Métrica

Dato cuantificable que mide un proceso.

Ejemplo:

* Número de visitantes
* Tasa de rebote

### Diferencia clave

| Métrica                 | KPI                        |
| ----------------------- | -------------------------- |
| Informativa             | Estratégico                |
| Puede no tener objetivo | Siempre tiene meta y plazo |
| Operativa               | Decisional                 |

Un dashboard sin KPIs claros genera “parálisis por análisis” 

---

# 🌟 9. Extensiones (Extra)

Las extensiones permiten añadir funcionalidades externas al dashboard:

* Integración con APIs
* Análisis avanzado
* Funcionalidades personalizadas

Se añaden desde:
`Objeto → Extensión`

Son un complemento avanzado para casos específicos 

---

# 🎓 Conclusión del Módulo

Después de esta lección eres capaz de:

* Crear dashboards interactivos
* Controlar visualizaciones con parámetros
* Construir métricas calculadas
* Aplicar funciones avanzadas
* Crear narrativas con historias
* Diseñar dashboards estratégicos con KPIs

El siguiente nivel ya no es solo hacer gráficos,
sino diseñar herramientas reales de decisión basadas en datos. 📊
