## Campos calculados / parametros creados

- Disponibilidad:
```
IF  [Availability 365] < 100 
THEN "POCA DISPONIBILIDAD"
ELSEIF  [Availability 365] > 100 
AND  [Availability 365] <= 200 
THEN "DISPONIBILIDAD MEDIA"
ELSE "DISPONIBILIDAD ALTA"
END
```

- Listings inactivos:
```
IF DATEDIFF("day", [Last Review], TODAY()) > 365 
THEN "Inactivo"
ELSE "Activo"
END
```

- Proximidad al centro:
```
IF [distancia al centro de Barcelona] <= 2 
THEN "Centro"
ELSEIF [distancia al centro de Barcelona] <= 5 
THEN "Zona Media"
ELSE "Periferia"
END
```

- distancia al centro de Barcelona:
```
DISTANCE(
    MAKEPOINT([Latitude], [Longitude]),
    MAKEPOINT(41.3874, 2.1686),
    "km"
)
```

- Parametros:
```
CASE [Precio/Disponibilidad] 
WHEN "Precio" THEN [Price]
WHEN  "Disponibilidad" THEN [Availability 365]
END
```

- Punto Geográfico:
```
MAKEPOINT([Latitude], [Longitude])
```

- Reviews por año
```
YEAR([Last Review])
```

- Filtro con imagen:
```
CASE [Room Type]
    WHEN "Entire home/apt" THEN 1
    WHEN "Hotel room" THEN 2
    WHEN "Private room" THEN 3
    WHEN "Shared room" THEN 4
    ELSE 0  
END

```

## Pasos para crear un campo calculado:
1. Click derecho en el panel de datos → Crear → Campo calculado
2. Escribir la fórmula
3. Click en OK
4. El nuevo campo aparecerá en el panel de datos y se podrá usar como cualquier grafico o filtro, o incluso en otros campos calculados.


## Pasos para crear un parámetro:
1. Click derecho en el panel de datos → Crear → Parámetro
2. Elegir el tipo de datos (número, fecha, cadena)
3. Elegir el rango de valores (todos, lista, rango)
4. Click en OK
5. El nuevo parámetro aparecerá en el panel de datos y se podrá usar en campos calculados o como filtro.
6. Si quieres que el usuario pueda interactuar con el parámetro, haz click derecho sobre el parámetro → Mostrar control de parámetro.


## Gáficos creados con campos calculados y parámetros con Airbnb Barcelona:

- Precio/disponibilidad por distrito
- Cantidad de alojamientos segun su disponibilidad
- Alojamientos activos e inactivos
- Ubicacion de los hoteles en el mapa
-  Scatterplot de precio vs distancia al centro de Barcelona
- Clasificación de los alojamientos segun su proximidad al centro de Barcelona