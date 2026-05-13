# Guia mecanica y flujo de trabajo - Proyecto HEMA

## Proposito
Esta guia define como trabajar el proyecto HEMA en su fase actual: diseno CAD, validacion mecanica y prototipado fisico del tobillo humanoide.

El objetivo es que dos personas puedan colaborar sin pisarse cambios, sin sobreescribir piezas y con una trazabilidad tecnica clara.

## Regla base de alcance
* Lo que vive en Fusion 360 es el modelo maestro.
* Lo que se sube al repositorio es la version controlada en STEP, PDF y notas tecnicas.
* El repositorio no debe convertirse en un archivo caotico de exportaciones no verificadas.

## Flujo de trabajo recomendado
### 1. Definir la tarea
Antes de abrir Fusion 360, la pieza o modificacion debe tener claro:
* problema mecanico a resolver
* pieza afectada
* riesgo tecnico
* criterio de exito

### Checklist operativa
Usa la lista de [CHECKLIST_OPERATIVA.md](CHECKLIST_OPERATIVA.md) antes de exportar cualquier nueva revision.
La idea es que la revision no dependa de memoria ni de revisiones informales.

### 2. Trabajar en una rama dedicada
Cada cambio mecanico debe desarrollarse en su propia rama.
* Una rama por pieza o por mejora concreta.
* No mezclar cambios de distintas zonas del robot en una sola entrega.

### 3. Exportar con version controlada
Nunca sobrescribir un STEP antiguo sin dejar rastro.
* Usar versionado explicito en el nombre del archivo.
* Mantener una secuencia clara: v1, v2, v3.
* Si una version queda descartada, no eliminarla sin documentarlo.

### 4. Registrar el cambio
Cada exportacion debe dejar nota en `01_Mechanical/DESIGN_LOG.md` con:
* que se modifico
* por que se modifico
* que problema tecnico corrige
* que queda pendiente de validar

### 5. Revisar antes de cerrar
Antes de aprobar una revision:
* comprobar interferencias
* revisar tolerancias
* verificar accesibilidad de tornillos y herramientas
* confirmar que el recorrido mecanico no bloquea

## Nomenclatura sugerida
Usar una convención simple y repetible:
* `HEMA_Pieza_v1.step`
* `HEMA_Pieza_v2.step`
* `HEMA_Conjunto_Tobillo_v3.step`

Para planos:
* `HEMA_Pieza_v1.pdf`
* `HEMA_Conjunto_Tobillo_v3.pdf`

## Reglas para evitar conflictos entre dos personas
* No editar el mismo subconjunto de Fusion 360 al mismo tiempo sin coordinacion previa.
* Si una persona modifica geometria estructural, la otra debe revisar tolerancias, ensamble o fabricacion, no tocar la misma pieza a la vez.
* Si hay dudas sobre la version correcta, se consulta el `DESIGN_LOG` antes de exportar otra revision.
* Nadie reemplaza archivos en silencio.

## Checklist tecnico antes de publicar una pieza
### Geometria
* ¿La pieza cumple su funcion mecanica?
* ¿Hay interferencias visibles con piezas vecinas?
* ¿La movilidad real coincide con el rango esperado?

### Fabricacion
* ¿La pieza se puede imprimir sin soportes excesivos?
* ¿La orientacion de impresion favorece la resistencia?
* ¿La tolerancia de ensamble esta justificada?

### Ensamble
* ¿Se puede montar con herramientas normales?
* ¿La tornilleria esta definida?
* ¿La pieza puede desmontarse para mantenimiento?

## Parametros de impresion 3D que deben documentarse
Para cada pieza estructural se debe registrar:
* material
* altura de capa
* numero de perímetros
* relleno
* soportes
* orientacion de impresion
* zona critica de carga

## Que debe existir en un hardware open-source serio
Este proyecto deberia terminar con al menos:
* guia de ensamblaje
* BOM mecanico completo
* parametros de impresion 3D
* tolerancias criticas
* vistas explotadas o subconjuntos
* protocolo de validacion del prototipo

## Orden de ataque recomendado
### Bloque 1: cierre mecanico
* resolver ajuste tubo PVC / alojamiento impreso
* definir abrazadera o sistema de retencion
* cerrar la tornilleria del tobillo

### Bloque 2: fabricacion
* fijar parametros de impresion
* verificar orientacion de carga
* preparar piezas para primer prototipo

### Bloque 3: validacion
* ensayo de carga estatica
* revision de juego mecanico
* control del desgaste inicial

## Criterio de calidad
La revision va bien si una persona externa puede responder sin adivinar:
* que pieza necesita
* como la imprime
* con que la ensambla
* que tolerancias son criticas
* como sabe si funciona o no

## Nota final
Mantener el proyecto simple no significa hacerlo superficial. Significa documentar solo lo necesario, pero hacerlo con rigor suficiente para que el conjunto sea reproducible y defendible tecnicamente.