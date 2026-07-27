

## 1.  Funciones basicas de DAX en editor de consultas de DAX


```dax
EVALUATE
FILTER(
    'Compraventa',
    YEAR('Compraventa'[Fecha]) = 2023
)
```
## 2. Crear el calendario
Aquí estamos creando calendario con columnas, es para crear lo que afecta a todo el calendario. 

```dax
Calendario =
VAR FechaInicio = MIN('Compraventa'[Fecha])
VAR FechaFin    = MAX('Compraventa'[Fecha])
RETURN
ADDCOLUMNS(
    CALENDAR(FechaInicio, FechaFin),
    "Año", YEAR([Date]),
    "Mes Nro", MONTH([Date]),
    "Mes", FORMAT([Date], "MMMM"),
    "Trimestre", "Q" & FORMAT([Date], "Q"),
    "DiaSemanaNro", WEEKDAY([Date], 2),
    "NombreDia", FORMAT([Date], "dddd"),
    "AñoMes", FORMAT([Date], "YYYY-MM")
)
```


### 3. Para el velocimetro

Aquí vamos a crear medidas para el velocimetro y poder mostrarlo bien

```dax
ventas_totales = CALCULATE(SUM(Compraventa[Total Vendido]), ALL(Compraventa)) 

num_años = CALCULATE(DISTINCTCOUNT(Calendario[Año]), ALL(Calendario))

media_ventas = Compraventa[ventas_totales]/[num_años] 
```

Pasos
1. Arrastrar el velocimetro y rellenarlo con la suma total del vendido
2.  Arrstra un segmnetador por año
3. En el velocimetro en el total vendido poner el máximo el total vendido de nuevo. 
4. Necesito un valor maximo que no quiero que se filtre, y ahi entra la medida. 
4. Hacer una medida para la media para ponr un indicador


## 4. Para el KPIS

Para comparar los KPis con el año anterior. 

```dax
Viviendas Vendidas =
SUM( 'Compraventa'[Total] )
```

```dax
Viviendas Vendidas Año Anterior =
CALCULATE(
    [Viviendas Vendidas],
    SAMEPERIODLASTYEAR( 'Calendario'[Date] )
)
```
