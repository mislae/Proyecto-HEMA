# Proyecto HEMA: Robot humanoide de 1 m

## Estado del proyecto
Proyecto HEMA esta actualmente en fase de diseno mecanico, bocetaje y validacion CAD 3D. El foco real del repositorio es el conjunto pie-tobillo y la estructura fisica necesaria para probar el primer prototipo.

En esta etapa no hay desarrollo de software activo ni integracion VR en el alcance principal. Esos temas quedan como roadmap futuro, pero no deben confundirse con el entregable actual.

## Enfoque tecnico actual
* **Mecanica principal:** articulacion de tobillo con sistema de varillas (pushrod linkage) para reducir masa no suspendida.
* **Rango de movimiento:** +/-25 grados de pitch en el tobillo.
* **Estructura:** piezas impresas en 3D en PETG o ABS, tubo estructural PVC de 20 mm, rodamientos 608ZZ y actuacion con MG995.
* **Objetivo inmediato:** validar geometria, tolerancias, interferencias y ensamblaje del primer conjunto fisico.

## Como revisar los modelos
Los entregables mecanicos estan organizados para revisarse desde un CAD o visor compatible:
* Abre los archivos `.step` en Fusion 360, FreeCAD u otro visor CAD compatible.
* Revisa los planos PDF en la carpeta de dibujos para comprender cotas, orientacion y referencias de ensamblaje.
* Compara cada pieza con su entrada en `01_Mechanical/DESIGN_LOG.md` para entender la justificacion tecnica de la revision.
* Si una pieza es impresa en 3D, revisa tambien `04_Revision_Proyecto/PARAMETROS_IMPRESION_3D.md`.
* Si la pieza forma parte del montaje fisico, revisa `04_Revision_Proyecto/GUIA_ENSAMBLAJE.md` antes de ensamblar.

### Ubicacion de archivos relevantes
* `01_Mechanical/CAD`: modelos 3D exportados en STEP.
* `01_Mechanical/Drawings`: planos tecnicos en PDF.
* `01_Mechanical/DESIGN_LOG.md`: bitacora de decisiones de ingenieria y cambios de version.
* `02_Electronics/BOM`: lista de materiales y componentes.
* `04_Revision_Proyecto`: guia de trabajo, checklist y documentacion operativa.

## Resumen de arquitectura mecanica
* **Servo principal:** MG995 para el accionamiento del tobillo.
* **Transmision:** linkage de varillas para desplazar el servo fuera de la zona de mayor inercia.
* **Apoyos:** rodamientos 608ZZ para giro suave en el eje de la articulacion.
* **Estructura tubular:** PVC de 20 mm como elemento de tibia durante prototipado rapido.

## Estado de validacion
* El diseno ya identifica una holgura critica entre el tubo de PVC y el alojamiento impreso.
* El siguiente paso es cerrar tolerancias, revisar interferencias y definir la sujecion final del tubo.
* El sistema aun debe validarse con prototipo fisico antes de considerar el diseno como cerrado.

## Estructura del repositorio
* `01_Mechanical`: CAD, planos y bitacora mecanica.
* `02_Electronics`: BOM y documentos de componentes.
* `03_Software`: carpeta reservada para el futuro desarrollo de control.
* `04_Revision_Proyecto`: revision tecnica, guia de trabajo, checklist y documentacion de apoyo.

## Politica de versionado CAD (oficial)
Para mantener trazabilidad y evitar sobrescrituras, cada exportacion de modelo 3D debe seguir este esquema.

### 1) Identificador fijo por pieza
Cada pieza tiene un ID permanente que no cambia entre versiones.
Ejemplos:
* `ANK-001`: socket de tibia
* `ANK-002`: balancin
* `ANK-003`: abrazadera PVC

### 2) Version semantica por archivo
Cada exportacion usa `vMayor.Menor.Parche`:
* **Mayor (X.0.0):** cambia funcion mecanica o interfaces de ensamble.
* **Menor (0.X.0):** ajusta tolerancias o cotas sin romper interfaces.
* **Parche (0.0.X):** correccion menor sin impacto funcional del conjunto.

### 3) Formato de nombre obligatorio
Usar este formato para STEP y planos asociados:
* `HEMA_[ID-Pieza]_[NombreCorto]_vX.Y.Z.step`
* `HEMA_[ID-Pieza]_[NombreCorto]_vX.Y.Z.pdf`

Ejemplo:
* `HEMA_ANK-001_socket-tibia_v2.1.0.step`

### 4) Reglas de publicacion
* Nunca sobrescribir una version anterior.
* Cada version nueva requiere una entrada en `01_Mechanical/DESIGN_LOG.md`.
* Si no pasa `04_Revision_Proyecto/CHECKLIST_OPERATIVA.md`, no se publica al repositorio.

### 5) Estructura sugerida por pieza
Para escalar el historico sin desorden:
* `01_Mechanical/CAD/ANK-001/`
* `01_Mechanical/CAD/ANK-002/`
* `01_Mechanical/CAD/ANK-003/`
Cada carpeta guarda todas las revisiones de la misma pieza.

## Roadmap inmediato
1. Cerrar tolerancias y fijacion del tobillo.
2. Completar BOM mecanico con tornilleria y elementos comerciales.
3. Definir parametros de impresion 3D por pieza.
4. Preparar un primer prototipo fisico para verificacion estatica.

## Nota para evaluadores
Este repositorio esta pensado para mostrar rigor de diseno mecanico, trazabilidad de decisiones y capacidad de prototipado. La calidad del proyecto se mide por la claridad del modelo, la reproducibilidad del ensamble y la validez de las decisiones de ingenieria.
