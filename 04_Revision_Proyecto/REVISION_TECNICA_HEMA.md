# Revision tecnica del Proyecto HEMA

## Estado actual
El repositorio esta bien encaminado para una fase de bocetaje y validacion mecanica, pero la documentacion todavia mezcla el alcance presente con funcionalidades futuras que hoy no forman parte del entregable principal.

La lectura tecnica del workspace es esta:
- El proyecto real esta centrado en el tobillo humanoide, la estructura mecanica y el prototipado fisico.
- El CAD ya existe al menos en una revision STEP y hay un plano PDF del conjunto pie-tobillo.
- El log de diseno ya registra decisiones relevantes, incluyendo el sistema de varillas, rodamientos 608ZZ, tubo PVC de 20 mm y el uso de MG995.
- Falta documentar con rigor el proceso de fabricacion, ensamblaje, tolerancias y validacion.

## Problema principal de documentacion
La documentacion no esta alineada al 100 por ciento con la fase actual del proyecto. En particular:
- El README sugiere una arquitectura con software, RPi y VR que hoy no corresponde al foco real.
- El BOM incluye componentes de etapa futura, lo que puede confundir a evaluadores o revisores.
- No existe una guia clara para fabricar, ensamblar y verificar las piezas mecanicas.

## Prioridad alta: issues tecnicas a atacar
### 1. Cierre de tolerancias del tobillo
El punto mas urgente es resolver el ajuste entre el tubo PVC y la pieza impresa.
- Se reporta una holgura de 1.3 mm entre el tubo y el alojamiento.
- Esa holgura debe convertirse en una decision de diseno concreta: ajuste por interferencia, abrazadera con tornillo, o retencion secundaria.
- Debe definirse el rango admisible de tolerancia de fabricacion para no depender de ajuste manual excesivo.

### 2. Dimensionamiento del tren servo-varillaje
La relacion mecanica del sistema debe validarse con calculo, no solo con intuicion de CAD.
- Verificar el par disponible del MG995 bajo la geometria real del linkage.
- Confirmar que la relacion de palancas entrega el momento necesario en el tobillo.
- Evaluar factor de seguridad bajo carga estatica y durante ciclos repetidos.

### 3. Tornilleria y elementos comerciales faltantes
El BOM esta incompleto para fabricacion real.
- Faltan tornillos, tuercas, arandelas, separadores, insertos termicos y fijadores de rosca.
- Tambien faltan elementos de retencion para rodamientos y criterios de montaje.
- Sin esto, el proyecto no es reproducible por terceros.

### 4. Estudios de interferencia y ensamblaje
Antes de producir mas piezas, conviene revisar interferencias en CAD.
- Verificar colisiones entre varillaje, servo, soporte impreso y tubo PVC.
- Revisar accesibilidad de herramienta para tornillos y mantenimiento.
- Validar que el recorrido de +/- 25 grados no genere rozamiento o bloqueo mecanico.

### 5. Parametros de impresion 3D
El proyecto requiere una base de fabricacion minima para las piezas estructurales.
- Definir material por pieza o familia de piezas: PETG o ABS segun carga y temperatura.
- Documentar orientacion de impresion, altura de capa, perimetros, infill y soportes.
- Indicar que zonas son criticas en direccion de capa para evitar delaminacion.

### 6. Protocolo de validacion mecanica
Falta una metodologia simple pero seria para probar el prototipo.
- Ensayo de carga estatica del tobillo.
- Medicion de deflexion y juego mecanico.
- Prueba de repetibilidad de movimiento.
- Inspeccion de desgaste en piezas impresas y uniones.

## Mejoras recomendadas para README
El README debe contar la historia correcta del proyecto.
- Dejar claro que el proyecto esta en fase de diseno CAD y validacion mecanica.
- Explicar como revisar los modelos: archivos STEP, PDFs de planos y renders si existen.
- Indicar la ubicacion de cada entregable mecanico.
- Mencionar el estado actual real y separar el roadmap futuro de software o VR.
- Evitar que el lector crea que el robot ya tiene una arquitectura completa de control.

## Mejoras recomendadas para CONTRIBUTING
El flujo de trabajo debe reducir el riesgo de sobreescritura y conflictos entre dos personas.
- Definir que Fusion 360 es la fuente maestra y que el repositorio solo recibe exports controlados.
- Usar nomenclatura estricta por pieza y version.
- Evitar que dos personas editen el mismo componente al mismo tiempo sin coordinacion.
- Exigir que cada nueva exportacion STEP vaya con una nota de cambio en el DESIGN_LOG.
- Separar claramente ramas de trabajo por objetivo mecanico.
- Agregar una regla de revision antes de reemplazar una version de pieza.

## Documentacion que falta en un hardware open-source serio
Hoy faltan varias piezas tipicas de un proyecto de hardware reproducible:
- Guia de ensamblaje paso a paso.
- Tabla de tornilleria y componentes comerciales.
- Parametros de impresion 3D por pieza.
- Criterios de tolerancia y ajuste para piezas impresas y comerciales.
- Vista explotada o esquema de subconjuntos.
- Criterios de inspeccion y prueba del prototipo.

## Propuesta de orden de trabajo
### Fase 1
- Cerrar tolerancias del tobillo.
- Completar la tornilleria y el BOM mecanico.
- Revisar interferencias y accesibilidad de ensamblaje.

### Fase 2
- Establecer parametros de impresion por pieza.
- Formalizar el design log como bitacora tecnica.
- Generar guia de ensamblaje basica.

### Fase 3
- Validar par, rigidez y repetibilidad con prototipo.
- Refinar el README para presentar el proyecto como portafolio tecnico.
- Dejar el roadmap de software como futuro y no como alcance actual.

## Criterio de calidad para la siguiente revision
La siguiente version del repositorio deberia permitir que alguien externo entienda, fabrique y ensamble el tobillo sin tener que adivinar:
- Que pieza va donde.
- Con que tornillos se arma.
- Que tolerancias son criticas.
- Como se imprime cada componente.
- Como se valida si la pieza cumple o no.

## Nota final
Para un portafolio de ingreso a programas de ingenieria, el valor no esta solo en el modelo 3D sino en la trazabilidad tecnica. Si ordenan la documentacion alrededor de la validacion mecanica, el proyecto se va a ver mucho mas serio y reproducible.