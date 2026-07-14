# 🗺️ Hoja de ruta I:  Fundamentos de Tableau

## 🎯 Objetivo general
Aprender a **cargar, revisar, preparar y publicar datos en Tableau**, entendiendo la herramienta y evitando errores comunes antes de crear visualizaciones y dashboards.

Esta hoja de ruta te acompaña paso a paso desde abrir Tableau por primera vez hasta publicar tu primer trabajo en Tableau Public.

---

## Fase 0 · ¿Por qué visualizamos datos?

### 🎯 Objetivo
Entender para qué sirve Tableau y por qué la visualización es clave en análisis de datos.

### 🧠 Ideas clave
- Visualizar datos no es “hacer gráficos bonitos”.
- Una buena visualización ayuda a:
  - entender qué está pasando,
  - detectar patrones,
  - tomar decisiones.
- Tableau es una herramienta para **contar historias con datos**.

✅ **Qué deberías entender al final**  
Que Tableau es una herramienta de análisis y comunicación, no solo de diseño.

---

## Fase 1 · Primer contacto con Tableau y su interfaz

### 🎯 Objetivo
Saber moverte por Tableau sin perderte.

### 🧠 Qué es importante aquí
Cuando abrimos Tableau encontramos varias zonas clave:

- **Página de inicio**
  - Conectar a datos
  - Abrir trabajos anteriores
  - Acceder a recursos de aprendizaje

- **Fuente de datos**
  - Donde se cargan y preparan los datos
  - Aquí revisamos si los datos están bien antes de analizarlos

- **Hojas de trabajo**
  - Donde se crean los gráficos individuales

- **Dashboards**
  - Donde juntamos varios gráficos en una sola pantalla

- **Historias**
  - Donde contamos una narrativa paso a paso con visualizaciones

📌 **Concepto importante**  
Un **libro de Tableau** puede contener:
- varias hojas,
- varios dashboards,
- varias historias.

✅ **Qué deberías saber hacer**  
Identificar cada parte de la interfaz y saber para qué sirve.

---

## Fase 2 · Carga de datos y verificación inicial

### 🎯 Objetivo
Cargar datos correctamente y comprobar que Tableau los ha interpretado bien.

### 🧠 Qué hacemos al cargar datos
- Conectamos archivos (CSV, Excel, etc.).
- Miramos la vista previa de los datos.
- Revisamos:
  - tipos de datos (texto, número, fecha),
  - valores nulos,
  - columnas raras o mal leídas.

📌 **Muy importante**  
Si los datos están mal cargados:
- los cálculos fallan,
- los gráficos salen mal,
- el análisis no es fiable.

✅ **Qué deberías saber hacer**  
Detectar si un campo debería ser número, fecha o texto y corregirlo.

**¿Qué podemos corregir si los datos no se han cargado bien?**
- Cambiar el tipo de dato manualmente.
- Ajustar la configuración regional (ver fase 3).
- Crear nuevas columnas calculadas para arreglar problemas.

---

## Fase 3 · Configuración regional y formatos

### 🎯 Objetivo
Evitar errores comunes con números y fechas.

### 🧠 Qué es la configuración regional
Define cómo Tableau interpreta:
- separadores decimales (coma o punto),
- separadores de miles,
- formatos de fecha,
- moneda.

### ⚠️ Problema típico
Un número aparece como texto → no se puede sumar ni usar en gráficos.

### 🛠️ Qué podemos hacer
- Cambiar la configuración regional del libro.
- Ajustar el formato de columnas concretas.

✅ **Qué deberías saber hacer**  
Reconocer cuándo un problema es de formato y saber cómo solucionarlo.

---

## Fase 4 · Preparación y combinación de datos

### 🎯 Objetivo
Trabajar con más de un fichero de datos.

### 🧠 Formas de trabajar con varios ficheros

#### 1️⃣ Fuentes de datos independientes
- Ficheros que no tienen relación entre sí.
- Se usan en hojas o dashboards distintos.

#### 2️⃣ JOIN (unir por columnas)
- Une datos que comparten una columna en común.
- Ejemplo: clientes + pedidos (ID cliente).

#### 3️⃣ UNION (concatenar por filas)
- Une ficheros con las mismas columnas.
- Ejemplo: ventas de varios meses.

📌 **Idea clave**
- JOIN = unir columnas relacionadas  
- UNION = apilar filas similares

✅ **Qué deberías saber hacer**  
Elegir correctamente entre JOIN o UNION según el caso.

---

## Fase 5 · Data Interpreter (intérprete de datos)

### 🎯 Objetivo
Limpiar automáticamente datos mal estructurados en Excel.

### 🧠 Qué hace el Data Interpreter
- Elimina filas vacías.
- Ignora títulos o notas extra.
- Ajusta tablas mal formateadas.

⚠️ **Importante**
- Ayuda, pero no sustituye una limpieza completa.
- Siempre hay que revisar el resultado.

✅ **Qué deberías saber hacer**  
Saber cuándo usarlo y revisar si el resultado es correcto.

---

## Fase 6 · Guardado de trabajo y estructura del libro

### 🎯 Objetivo
Organizar bien tu trabajo en Tableau.

### 🧠 Buenas prácticas
- Usar nombres claros para hojas y dashboards.
- Guardar versiones intermedias.
- Mantener el libro ordenado.

✅ **Qué deberías saber hacer**  
Guardar y estructurar correctamente un proyecto de Tableau.

---

## Fase 7 · Publicar en Tableau Public

### 🎯 Objetivo
Compartir tu trabajo y usar Tableau como portfolio.

### 🧠 Qué es Tableau Public
- Plataforma online para publicar visualizaciones.
- Todo lo que subes es público.

### ⚠️ Importante
- No subir datos sensibles.
- Revisar antes de publicar.

✅ **Qué deberías saber hacer**  
Publicar un libro en Tableau Public y compartir el enlace.

---

## Fase 8 · Inspiración: Viz of the Day

### 🎯 Objetivo
Aprender viendo buenas visualizaciones.

### 🧠 Qué es la Viz of the Day
- Visualizaciones destacadas creadas por la comunidad.
- Fuente de inspiración y aprendizaje.

### 🔍 Qué analizar
- Tipo de gráfico.
- Uso del color.
- Claridad del mensaje.
- Interactividad.

📌 **Aprender copiando está bien**
Analizar visualizaciones de otras personas es una forma excelente de aprender.

✅ **Qué deberías saber hacer**  
Mirar visualizaciones con criterio y sacar ideas para las tuyas.

---

> Una buena visualización empieza **mucho antes del gráfico**.
