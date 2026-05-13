# Bill of Materials (BOM) - Proyecto HEMA

## Alcance actual
Este BOM esta centrado en la fase mecanica y de prototipado fisico del tobillo humanoide. Los elementos de software, teleoperacion y VR quedan fuera del alcance activo de esta revision.

## Componentes confirmados
| Componente               | Cantidad | Funcion principal                                        |  Estado   |
| :----------------------- | :------: | :------------------------------------------------------- | :-------: |
| **Servo MG995**          |    1     | Actuador principal del tobillo.                          | Adquirido |
| **Rodamiento 608ZZ**     |    2     | Pivotes de baja friccion para la articulacion.           | Adquirido |
| **Tubo PVC 20 mm**       |   1 m    | Estructura principal de la tibia durante el prototipado. | Adquirido |
| **Filamento PETG o ABS** |   1 kg   | Impresion 3D de piezas estructurales y soportes.         | Pendiente |

## Componentes mecanicos por definir
| Componente                         | Cantidad | Funcion principal                                                |  Estado   |
| :--------------------------------- | :------: | :--------------------------------------------------------------- | :-------: |
| **Tornillos M3 cabeza cilíndrica** |    8     | Union general de soportes impresos y piezas de carcasa.          | Pendiente |
| **Tornillos M3 avellanados**       |    4     | Cierre de tapas o piezas donde la cabeza no debe sobresalir.     | Pendiente |
| **Tornillos M4 para clamp**        |    2     | Cierre de abrazadera del tubo PVC.                               | Pendiente |
| **Tuercas autoblocantes M3**       |    8     | Retencion de uniones con vibracion.                              | Pendiente |
| **Tuercas M4 autoblocantes**       |    2     | Retencion del sistema de abrazadera.                             | Pendiente |
| **Arandelas planas M3**            |    16    | Distribucion de carga y separacion.                              | Pendiente |
| **Arandelas planas M4**            |    4     | Apoyo en la abrazadera del tubo PVC.                             | Pendiente |
| **Insertos termicos M3**           |    6     | Rosca metalica en piezas impresas.                               | Pendiente |
| **Fijador de roscas medio**        |    1     | Prevencion de aflojamiento por vibracion.                        | Pendiente |
| **Pasador o eje secundario 8 mm**  |    1     | Retencion o guia de componentes moviles segun el conjunto final. | Pendiente |

## Componentes fuera del alcance activo
| Componente            | Cantidad | Funcion principal                           | Estado |
| :-------------------- | :------: | :------------------------------------------ | :----: |
| **Raspberry Pi 4B**   |    1     | Control de alto nivel y logica de software. | Futuro |
| **Raspberry Pi Pico** |    1     | Control de bajo nivel y PWM.                | Futuro |
| **Meta Quest 3S**     |    1     | Teleoperacion y VR.                         | Futuro |

## Observaciones tecnicas
* El BOM mecanico debe cerrarse antes de fabricar una nueva iteracion del tobillo.
* La tornilleria y los elementos de retencion no pueden quedar como decisiones informales.
* Cada pieza comercial debe quedar ligada a una referencia concreta en CAD o en la guia de ensamblaje.
* Las cantidades anteriores son preliminares y deben ajustarse al ensamblaje final antes de comprar lote completo.
