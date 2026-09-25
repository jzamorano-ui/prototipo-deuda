# Prototipo · Deuda del periodo

Prototipo navegable de la sección **Deuda** del backoffice de Recaudación.
Reproduce el diseño de Figma (`RC-Gestión deuda`) como HTML funcional, para
poder recorrer el flujo en vez de mirar pantallas estáticas.

**Ver el prototipo:** https://jzamorano-ui.github.io/prototipo-deuda/

## Qué se puede hacer

Elige un periodo en el selector. Cada opción muestra una situación distinta:

| Periodo | Situación |
|---|---|
| Septiembre 2026 | Periodo en curso, deuda preliminar |
| Septiembre 2026 (inconsistencias) | Con registros por revisar y su panel de detalle |
| Agosto 2026 | Periodo cerrado, deuda final — el recorrido principal |
| Julio 2026 · Junio 2026 | Periodos cerrados anteriores |

Desde ahí: **Ver filtros** abre la búsqueda, **Exportar deuda** descarga,
los ⓘ de la cabecera explican su columna, y la tabla desplaza en horizontal
manteniendo fija la identidad del cotizante.

## Lo que el prototipo muestra y el diseño estático no

- La carga se siente distinta según el periodo: un mes cerrado **se consulta**
  y entra con skeleton; el mes en curso **se calcula** y usa loader con mensaje.
- Los filtros filtran de verdad y recalculan el paginador; los totales del
  periodo no cambian.
- El truncado, el scroll horizontal y los tooltips solo se evalúan usándolos.

## Sobre los datos

Todos los datos son de muestra. Los RUT, nombres y montos son ficticios.
Las cifras de Julio y Junio son de ejemplo: el diseño solo define datos para
Agosto y Septiembre.

## Tipografía

La interfaz está tipografiada en **Interstate**, que es licencia comercial y no
se distribuye acá. Quien no la tenga instalada verá el prototipo con Archivo,
que es algo más ancha, así que algunas columnas quedan más justas de lo previsto.

## Archivos

- `happy-path-deuda.html` — el prototipo, autocontenido salvo la fuente
- `logo-esencial.png` · `avatar.png` — exportados del archivo de diseño
