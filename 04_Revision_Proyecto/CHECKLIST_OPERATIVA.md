# Checklist operativa - Proyecto HEMA

## Antes de abrir Fusion 360
- [ ] La pieza o cambio esta definido con una necesidad mecanica concreta.
- [ ] La zona del robot afectada esta identificada.
- [ ] El riesgo tecnico principal esta escrito en una frase.
- [ ] El criterio de exito esta claro.

## Antes de exportar un STEP
- [ ] La geometria nueva fue revisada con la version anterior.
- [ ] No hay interferencias evidentes con piezas vecinas.
- [ ] El recorrido mecanico completo es posible sin bloqueo.
- [ ] La solucion de retention o sujecion esta resuelta.
- [ ] La tolerancia de ensamble esta justificada.

## Antes de publicar una nueva revision
- [ ] El archivo tiene version explicita en el nombre.
- [ ] El cambio quedo registrado en `01_Mechanical/DESIGN_LOG.md`.
- [ ] Se guardo una nota de por que se cambio la pieza.
- [ ] Se indico que queda pendiente de validar.
- [ ] El STEP anterior no fue sobrescrito sin trazabilidad.

## Antes de comprar o fabricar
- [ ] La tornilleria asociada esta definida.
- [ ] Los materiales necesarios estan en el BOM.
- [ ] Los parametros de impresion 3D estan documentados o al menos definidos.
- [ ] La pieza puede montarse y desmontarse con herramientas normales.
- [ ] La fabricacion no depende de ajustes improvisados.

## Antes de cerrar la iteracion
- [ ] El cambio mejora una variable mecanica real.
- [ ] La solucion sigue siendo simple de fabricar para un equipo pequeno.
- [ ] El prototipo puede evaluarse sin redisenar todo el conjunto.
- [ ] El siguiente paso tecnico esta escrito.

## Regla final
Si una casilla critica queda sin marcar, la pieza no se publica como version final.
