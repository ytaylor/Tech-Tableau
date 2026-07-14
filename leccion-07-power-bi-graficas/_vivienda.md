## Transformaciones Datasets Viviendas:

Vamos a hacer estas transformaciones en Power Query sobre el conjunto de datos de las Viviendas
### Crear columana Periodo en Valor Tasado

- Seleccionar columna Año y Periodo, luego ir a Agregar columna > Combinar Columnas. 
- Renombrar la nueva columna a "Periodo".


### Crear columna Fecha en todo el Datasets

1. Agregar una columna personalizada con el siguiente código:

```m

#date(
    Number.From(Text.Start([Periodo], 4)),
    (Number.From(Text.End([Periodo], 1)) - 1) * 3 + 1,
    1
)
```
- Para las fechas con mes
```
try #date(
    Number.FromText(Text.Start(Text.Trim([Periodo]), 4)),
    Number.FromText(Text.PadStart(Text.AfterDelimiter(Text.Trim(Text.Upper([Periodo])), "M"), 2, "0")),
    1
) otherwise null
```

2. Renombrar la columna a "Fecha".
3. Cambiar el tipo de datos de la columna "Fecha" a fecha.

## Otras transformaciones:

1. Separa comunidad autónoma y numero siempr
2. Reemplaza los valores de la columna "Comunidad Autónoma", las comas por espacios en blanco.
3. Cambia el tipo de datos de Comunidad Autonoma a Region y Pais. 
4. Elimina las columnas Número, Trimestre cuando sea necesario.
5. Filtrar para quedarnos solo con las comunidades autónomas de las alumnas. 

## Graficos a realizar:
- Graficos de barras para comparar el valor tasado entre comunidades autónomas: Promeedio de Valor Tasado por Comunidad Autónoma.
- Graficos de líneas para mostrar la evolución del valor tasado a lo largo del tiempo. 
- Graficos de líneas para mostrar la evolución del valor tasado a lo largo del tiempo por comunidad autónoma.
- Grafico de lineas para mostrar la cantida de viviendas de primera y segunda mano vendidas a lo largo del tiempo.
- Mapa para visualizar la distribución geográfica del valor tasado por comunidad autónoma.
    - En este caso pasa que muestra ciudades en otros sitios, vamoa a crear una nueva columna para el pais: 
        - Modelado > Nueva columna > Pais = "España"  
- Big Numbers: 
    - promedia del valor tasado en el periodo disponible.
    - Promedio del indice de variación interanual en el periodo disponible.
    - Total de ventas realizadas en el periodo disponible.
    - Tarjeta de big number
- Grafico de barras agrupadas para mostrar la cantida de viviendas de primera y segunda mano vendidas por comunidad autónoma.
- Grafico embudo para mostrar el proceso de compraventa de viviendas: Total de viviendas en el mercado, Total de viviendas vendidas, Total de viviendas nuevas vs usadas vendidas.
- Esquema Jerárquico para mostrar la relación entre comunidades autónomas, provincias y tipo de vivienda.
- Grafico de cintas

# Segmentos e interacciones entre gráficos:
- Filtro por comunidad autónoma.
- Filtro por periodo (año o trimestre).
- Filtro por tipo de vivienda (primera mano, segunda mano).

