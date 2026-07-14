

## 🔵 RELACIONES VIRTUALES (TREATAS, CROSSFILTER, USERELATIONSHIP)

| Función | ¿Qué hace? | ¿Cuándo la usas? |
| :--- | :--- | :--- |
| **USERELATIONSHIP** | **Enciende** una relación. | Cuando tienes una **línea punteada** (inactiva) y quieres usarla. |
| **CROSSFILTER** | **Apaga** o cambia una relación. | Cuando quieres que una **línea sólida** deje de filtrar para un cálculo. |
| **TREATAS** | **Inventa** una relación. | Cuando **no hay ninguna línea** entre las tablas pero quieres que se filtren. |

### En resumen:
*   **USERELATIONSHIP:** Usa la línea punteada.
*   **CROSSFILTER:** Ignora la línea sólida.
*   **TREATAS:** Crea una línea invisible.


### 🚀 TREATAS → Relacionar “Comunidad Autónoma” entre 2 tablas sin crear una relación física

Digamos que quieres ver:

**Valor tasado m² por CCAA**  
pero filtrado por selección de la tabla **valor_m2_provincias**.

```dax
Indice por CCAA Virtual = 
VAR ComunidadSeleccionada = VALUES('valor_m2_ccaa'[Comunidad_Autonoma])
RETURN
CALCULATE(
    AVERAGE('variación_de_precios'[Indice_Precio]),
    TREATAS(ComunidadSeleccionada, 'variación_de_precios'[CA])
)
```

⚡ **Sin crear relaciones en el modelo.**

---

### 🚀 CROSSFILTER → Ignorar o cambiar dirección del filtro  

Ejemplo: quieres sumar ventas sin que el filtro de CCAA afecte:

```dax
Total Nacional (Sin Filtro Fecha) = 
CALCULATE(
    SUM('Compraventa'[Total]),
    CROSSFILTER('Calendario'[Date], 'Compraventa'[Fecha], None)
)
```