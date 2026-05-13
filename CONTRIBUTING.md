# Guía de Contribución - Proyecto HEMA

Esta guía existe para que dos personas puedan trabajar sobre Fusion 360 y el repositorio sin sobreescribir versiones ni perder trazabilidad tecnica.

## 1. Alcance de trabajo
* El modelo maestro vive en Fusion 360.
* El repositorio recibe exportaciones controladas en `.step`, `.pdf` y notas tecnicas.
* No subas exportaciones intermedias sin justificar por qué son necesarias.

## 2. Nomenclatura de archivos CAD
* Nunca sobrescribas un archivo `.step` anterior.
* Usa versionado explicito: `HEMA_Pieza_v1.step`, `HEMA_Pieza_v2.step`.
* Si existe un plano asociado, versiona tambien el PDF con el mismo criterio.
* Cada nueva exportacion debe quedar registrada en `01_Mechanical/DESIGN_LOG.md`.

## 3. Flujo de trabajo para Fusion 360
* Antes de editar una pieza, confirma quien la tiene asignada.
* Si dos personas necesitan intervenir el mismo subconjunto, una edita y la otra revisa.
* No mezcles cambios de geometria, tolerancia y ensamble en una sola revision si no es necesario.
* Exporta solo cuando el cambio tenga una decision tecnica clara y validable.

## 4. Reglas para evitar conflictos de version
* Nunca reemplaces un STEP en silencio.
* Mantén una secuencia ordenada de revisiones.
* Si una version queda descartada, deja trazabilidad en el `DESIGN_LOG` y no elimines el historial sin acuerdo.
* Si hay duda sobre la revision correcta, se prioriza la version mas reciente validada en el log.

## 5. Ramas de trabajo
* Nunca trabajes directamente en `main`.
* Crea una rama por cambio mecanico concreto.
* Usa nombres descriptivos como `mecanica-abrazadera`, `tobillo-v5` o `revision-bom-fasteners`.
* No mezcles en una misma rama cambios que afecten piezas no relacionadas.

## 6. Revision antes de publicar
Antes de cerrar una pieza o subir una nueva version, verifica:
* interferencias visibles con piezas vecinas
* tolerancias de ensamble
* accesibilidad para herramientas
* recorrido mecanico completo
* coherencia con el BOM y la guia de ensamblaje

## 7. Documentacion obligatoria
Para el trabajo mecanico actual, revisa y actualiza segun corresponda:
* `01_Mechanical/DESIGN_LOG.md` para decisiones tecnicas
* `02_Electronics/BOM/BOM.md` para materiales y tornilleria
* `04_Revision_Proyecto/CHECKLIST_OPERATIVA.md` antes de exportar o cerrar una revision
* `04_Revision_Proyecto/GUIA_ENSAMBLAJE.md` si el cambio afecta el montaje fisico

## 8. Notas sobre software
La documentacion de software quedara para la fase correspondiente. Si se retoma, el codigo de la RPi Pico ira en `/03_Software/MicroPython` y el de la RPi 4B en `/03_Software/Python_Main`.

## 9. Regla final
Si un cambio no puede explicarse en una frase tecnica clara, todavia no esta listo para versionarse.
