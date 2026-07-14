

## 1.  Funciones basicas de DAX en editor de consultas de DAX

```dax
EVALUATE
'Calendario'
```

```dax
EVALUATE
FILTER(
    'Compraventa',
    YEAR('Compraventa'[Fecha]) = 2023
)
```
```dax
EVALUATE
SUMMARIZECOLUMNS(
    'Calendario'[Trimestre],
    "Total Ventas", SUM('Compraventa'[Importe]) -- Cambia [Importe] por tu columna de valor
)
ORDER BY 'Calendario'[Trimestre] ASC
```

```dax
EVALUATE
CALCULATETABLE(
    'Compraventa',
    'Calendario'[DiaSemanaNro] IN {6, 7}
)
```
## 2. Crear el calendario
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

```dax
ventas_totales = CALCULATE(SUM(Compraventa[Total Vendido]), ALL(Compraventa)) 

num_años = CALCULATE(DISTINCTCOUNT(Calendario[Año]), ALL(Calendario))

media_ventas = Compraventa[ventas_totales]/[num_años] 
```

## 4. Para el KPIS

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
