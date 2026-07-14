
### 1. Funciones básicas de fecha

Estas se usan mucho para construir la tabla calendario y columnas calculadas:

- `YEAR(Fecha)` → devuelve el año.  
  ```dax
  Año = YEAR('Calendario'[Date])
  ```

- `MONTH(Fecha)` → número de mes (1–12).  
  ```dax
  Mes Nro = MONTH('Calendario'[Date])
  ```

- `DAY(Fecha)` → día del mes (1–31).  
  ```dax
  Día = DAY('Calendario'[Date])
  ```

- `WEEKDAY(Fecha, [tipo])` → día de la semana como número.  
  ```dax
  DiaSemanaNro = WEEKDAY('Calendario'[Date], 2)   -- 2 = lunes=1, domingo=7
  ```

- `FORMAT(Valor, "patrón")` → da formato de texto a fechas.  
  ```dax
  MesNombre = FORMAT('Calendario'[Date], "MMMM")      -- “enero”
  NombreDia = FORMAT('Calendario'[Date], "dddd")      -- “lunes”
  AñoMes    = FORMAT('Calendario'[Date], "YYYY-MM")   -- “2024-01”
  ```

- `DATE(Año, Mes, Día)` → construye una fecha desde números.  
  ```dax
  Inicio2024 = DATE(2024, 1, 1)
  ```

---

### 2. Funciones para inteligencia de tiempo (Time Intelligence)

Funcionan mejor cuando ya tienes una **tabla calendario** marcada como tabla de fechas.

- `TODAY()` → la fecha de hoy.  
  ```dax
  Ventas Hasta Hoy = CALCULATE( SUM(Ventas[Importe]), FILTER( ALL('Calendario'), 'Calendario'[Date] <= TODAY() ) )
  ```

- `DATEADD(TablaFechas[Fecha], n, intervalo)`  
  Desplaza el rango de fechas.  
  ```dax
  Ventas Año Pasado =
  CALCULATE(
      SUM(Ventas[Importe]),
      DATEADD('Calendario'[Date], -1, YEAR)
  )
  ```

- `SAMEPERIODLASTYEAR(TablaFechas[Fecha])`  
  Mismo periodo pero un año antes.  
  ```dax
  Ventas Mismo Periodo Año Anterior =
  CALCULATE(
      SUM(Ventas[Importe]),
      SAMEPERIODLASTYEAR('Calendario'[Date])
  )
  ```

- `PARALLELPERIOD(TablaFechas[Fecha], n, intervalo)`  
  Similar a `DATEADD`, útil para comparar periodos paralelos.  
  ```dax
  Ventas 3 Meses Antes =
  CALCULATE(
      SUM(Ventas[Importe]),
      PARALLELPERIOD('Calendario'[Date], -3, MONTH)
  )
  ```

- `TOTALYTD(Expresión, TablaFechas[Fecha])`  
  Acumulado desde inicio de año hasta el contexto actual.  
  ```dax
  Ventas YTD =
  TOTALYTD(
      SUM(Ventas[Importe]),
      'Calendario'[Date]
  )
  ```

- `TOTALMTD`, `TOTALQTD` → igual que YTD pero mensual o trimestral.

---

### 3. Funciones para trabajar con periodos

- `STARTOFMONTH`, `ENDOFMONTH`, `STARTOFYEAR`, `ENDOFYEAR`, `STARTOFQUARTER`, `ENDOFQUARTER`  
  Devuelven la primera/última fecha del periodo en el contexto actual.

  ```dax
  Fecha Inicio Mes = FIRSTDATE( 'Calendario'[Date] )
  Fecha Fin Mes    = LASTDATE( 'Calendario'[Date] )
  ```

- `FIRSTDATE`, `LASTDATE`  
  Primera y última fecha del rango actual (por ejemplo, el mes filtrado).

---

### 4. Ejemplo de calendario “completo” aprovechando varias

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

