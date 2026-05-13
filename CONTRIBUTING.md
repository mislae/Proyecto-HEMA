# Guía de Contribución - Proyecto HEMA

¡Bienvenido al equipo de desarrollo! Para mantener el orden entre el diseño CAD y el código, sigue estas reglas:

## 1. Nomenclatura de Archivos CAD (Fusion 360)
*   Nunca sobrescribas un archivo `.step` antiguo. 
*   Usa el formato de versiones: `HEMA_Pieza_v1.step`, `HEMA_Pieza_v2.step`.
*   Añade siempre un comentario en el `DESIGN_LOG.md` explicando qué cambió en la nueva versión.

## 2. Reglas para el Código (Software)
*   El código de la RPi Pico va en `/03_Software/MicroPython`.
*   El código de la RPi 4B va en `/03_Software/Python_Main`.
*   Asegúrate de tener instalado el Workspace de VS Code (`.vscode/extensions.json`) antes de programar para mantener el mismo formato.

## 3. Uso de Ramas (Branches)
*   **Nunca trabajes directamente en la rama `main`.**
*   Crea una rama nueva para tu tarea (ej. `mecanica-abrazadera` o `codigo-pwm-servo`).