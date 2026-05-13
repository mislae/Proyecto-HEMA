# Parametros de impresion 3D - Proyecto HEMA

## Proposito
Este documento define el minimo tecnico que debe registrarse para imprimir piezas estructurales del Proyecto HEMA.

## Regla base
Cada pieza importante debe imprimirse con parametros conocidos y repetibles. No basta con decir "PETG" o "ABS"; hay que poder reproducir la pieza con el mismo comportamiento mecanico.

## Campos que deben documentarse por pieza
- Material
- Altura de capa
- Numero de perímetros
- Relleno
- Porcentaje de relleno
- Tipo de soportes
- Orientacion de impresion
- Temperatura de boquilla
- Temperatura de cama
- Zona critica de carga
- Observaciones de postproceso

## Recomendacion de documentacion minima
Para cada pieza estructural, registrar al menos:
- nombre de la pieza
- version
- material usado
- orientacion de impresion
- razon de esa orientacion
- si requiere soportes o no
- ajuste esperado con piezas comerciales

## Piezas que requieren mas cuidado
- Alojamiento del tubo PVC
- Soporte del tobillo
- Brazos de linkage
- Soportes del servo
- Cualquier pieza que reciba carga concentrada o vibracion repetida

## Buenas practicas
- Orientar las capas para que no trabajen en la direccion mas debil de la pieza.
- Evitar soportes innecesarios en superficies funcionales.
- Preferir geometria simple si reduce riesgo de delaminacion.
- Hacer una prueba corta si se cambia material o relleno.

## Criterio de decision
Si una pieza es estructural y soporta carga, su configuracion de impresion debe quedar escrita antes de fabricar el lote final.