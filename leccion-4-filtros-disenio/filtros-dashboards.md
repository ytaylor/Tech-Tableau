
# 📊  Interacción y Experiencia en Dashboards

En esta lección aprendemos a **enriquecer dashboards** en Tableau mediante:

* Filtros.
* Mapas.
* Tooltips personalizados.
* Elementos visuales (imágenes, botones, textos, contenedores).

El objetivo es pasar de dashboards estáticos a **dashboards interactivos y más profesionales**.

---

# Filtros

Un filtro permite **limitar los datos que se muestran** en una visualización.

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

---

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

---

# 🎓 Buenas prácticas

* Usar interactividad con intención.
* Mantener coherencia visual.
* No sobrecargar el dashboard.
* Guiar al usuario en la navegación.
* Probar la experiencia como si fueras el usuario final.
