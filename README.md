# Prototipo · Deuda de cotizaciones

Prototipo navegable del módulo **Cobranza › Deuda de cotizaciones**, fase 1
(deuda flujo). Reproduce el diseño de Figma (`RC-Gestión deuda`, sección
«Generación deuda») como HTML funcional, para recorrer los flujos en vez de
mirar pantallas estáticas.

## Qué se puede hacer

Elige un periodo en el selector y presiona **Seleccionar**:

| Periodo | Situación |
|---|---|
| Septiembre 2026 (en curso) | Deuda preliminar: se genera con loader. El recorrido principal |
| Septiembre 2026 (cerrado) | El mismo mes recién cerrado: se genera por primera vez, mismos montos |
| Septiembre 2026 (inconsistencias) | Registros por revisar y su panel de detalle (solo visualización) |
| Agosto 2026 · Julio 2026 · Junio 2026 | Meses ya cerrados: se consultan y entran con skeleton |

Las tres variantes de Septiembre existen para mostrarlas sin cambiar de mes;
en la plataforma solo existe una a la vez.

Desde ahí:

- **Pestañas Afiliados y Pagadores.** Al cambiar, la tabla entra con skeleton.
- **Ver filtros.** Cada pestaña tiene sus filtros y los chips muestran el conteo.
- **Exportar.** Dos opciones: deuda consolidada y la de la pestaña activa.
- **Menú ⋮ de cada fila.**
  - Afiliados: Ver pagos asociados, Ver EEPC relacionadas y Agregar o Ver marca.
  - Pagadores: Detalle de pago y Detalle de cotizaciones. Un pagador NN solo
    tiene Detalle de pago: no figura en el contrato, así que no tiene
    cotizaciones ni deuda que detallar.
- **Marca (Especial o Reputacional).** Se agrega, se ve y se edita. El detalle guarda el
  historial de observaciones con nombre, fecha y hora; la tabla muestra la
  más reciente.

## Reglas que el prototipo aplica

- **Tabla.** Ocupa el ancho disponible; si no cabe, hay scroll horizontal con
  la primera columna y Acciones fijas, y su sombra aparece solo cuando hay
  columnas pasando por debajo.
- **Cierre de modales.**
  - Consulta: se cierran con ✕, Esc o un clic fuera.
  - Con acciones (filtros y marca): se cierran con sus botones, sin ✕. Un clic
    fuera no los cierra y Esc equivale a Cancelar.
- **Montos.** Van en $ y en UF (3 decimales, UF a $38.489); los ceros se ven
  como «$0 / 0,000 UF» y lo que no aplica, como «—». Los periodos se muestran
  como mes y año («Agosto 2026»); las fechas reales, como la de pago, en
  dd/mm/aaaa.
- **Cuadre de los datos.** Lo pagado por cada afiliado es la suma de sus
  pagadores (incluidos los NN). Detalle de cotizaciones muestra solo los
  afiliados con deuda de ese pagador.

## Sobre los datos

Todos los datos son de muestra; los RUT, nombres y montos son ficticios.
Agosto y Septiembre usan las cifras del diseño. Julio y Junio son de ejemplo,
con los mismos afiliados de Agosto.

Después de los seis afiliados del diseño hay 60 más de relleno, para que
«Mostrar por página» con 25 o 50 muestre filas distintas. No cambian los
totales ni los conteos de los filtros.

## Tipografía

La interfaz está tipografiada en **Interstate**, que es licencia comercial y no
se distribuye acá. Quien no la tenga instalada verá el prototipo con Archivo,
que es algo más ancha.

## Archivos

- `happy-path-deuda.html`: el prototipo, autocontenido salvo la fuente.
- `logo-esencial.png` y `avatar.png`: exportados del archivo de diseño.
