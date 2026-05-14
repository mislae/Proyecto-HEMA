# Plan de ataque de 4 semanas - Proyecto HEMA

## Objetivo
Convertir el conjunto pie-tobillo en un prototipo mecanico reproducible, con tolerancias, ensamble y validacion minima cerrados.

## Tablero Kanban (seguimiento rapido)

| ID | Tarea | Responsable | Estado |
| :-- | :-- | :-- | :-- |
| W1-01 | Resolver holgura PVC-alojamiento | Martin / Companero | Todo |
| W1-02 | Definir retencion final (abrazadera/interferencia/hibrido) | Martin / Companero | Todo |
| W1-03 | Verificar recorrido completo sin interferencias | Martin / Companero | Todo |
| W2-01 | Cerrar tornilleria real en BOM | Martin / Companero | Todo |
| W2-02 | Definir parametros de impresion por pieza | Martin / Companero | Todo |
| W2-03 | Imprimir primera tanda de piezas | Martin / Companero | Todo |
| W3-01 | Ensamblar subconjunto pie-tobillo | Martin / Companero | Todo |
| W3-02 | Registrar incidencias de montaje | Martin / Companero | Todo |
| W3-03 | Corregir geometria por ajustes forzados | Martin / Companero | Todo |
| W4-01 | Ejecutar ensayo estatico de carga | Martin / Companero | Todo |
| W4-02 | Validar repetibilidad de movimiento | Martin / Companero | Todo |
| W4-03 | Revisar holguras y desgaste inicial | Martin / Companero | Todo |

Estados sugeridos: `Todo`, `Doing`, `Done`, `Blocked`.

## Reglas de uso del tablero
- Actualizar estado al cierre de cada jornada, no solo al final de la semana.
- Si una tarea queda en `Blocked`, anotar causa y siguiente accion en `01_Mechanical/DESIGN_LOG.md`.
- Si una tarea pasa a `Done`, verificar que tenga evidencia (STEP, BOM, nota tecnica o registro de prueba).
- No abrir tareas nuevas sin cerrar o desbloquear las criticas de la semana actual.

## Semana 1: Cierre de geometria critica
- Resolver holgura PVC-alojamiento.
- Definir estrategia de retencion final (abrazadera, interferencia o hibrido).
- Verificar recorrido completo del tobillo sin interferencias.
- Salida esperada: nuevo STEP de conjunto y nota tecnica en DESIGN_LOG.

## Semana 2: Tornilleria y fabricacion
- Cerrar lista de tornilleria real en BOM.
- Definir parametros de impresion para piezas estructurales.
- Imprimir primera tanda de piezas del tobillo.
- Salida esperada: BOM actualizado y registro de impresion por pieza.

## Semana 3: Ensamble y correcciones
- Ensamblar subconjunto completo pie-tobillo.
- Levantar incidencias de montaje y accesibilidad de herramientas.
- Corregir geometria si aparecen ajustes forzados.
- Salida esperada: guia de ensamblaje con observaciones reales del prototipo.

## Semana 4: Validacion mecanica minima
- Ensayo estatico de carga.
- Repetibilidad de movimiento en el rango objetivo.
- Revision de holguras y desgaste inicial.
- Salida esperada: estado de validacion documentado y decision de siguiente iteracion.

## Criterio de exito
Al final de la semana 4, una persona externa debe poder:
- entender que piezas fabricar,
- ensamblarlas sin improvisar,
- y evaluar si el conjunto cumple o no con criterios basicos.
