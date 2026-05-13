# Software & Control Roadmap - Proyecto HEMA

Este módulo gestiona la inteligencia y el movimiento del robot, utilizando una arquitectura híbrida entre procesamiento de alto nivel (RPi 4B) y control de tiempo real (RPi Pico).

## 🧠 Control Architecture

*   **High-Level Logic (Raspberry Pi 4B):** Encargada de la visión computacional, cinemática inversa y la interfaz de teleoperación con **Meta Quest 3S**.
*   **Low-Level Actuation (Raspberry Pi Pico):** Encargada de la generación de señales PWM para los servos MG995 y la lectura de sensores locales.

---

## 🚀 Development Phases

### Phase 1: Basic Motion & PWM (Current)
*   **Target:** Raspberry Pi Pico.
*   **Tasks:**
    *   Implementación de drivers básicos en **MicroPython** para el control de posición de servos.
    *   Calibración del rango de movimiento del tobillo ($\pm 25^\circ$).
    *   Pruebas de torque estático bajo carga del frame de 1 metro.

### Phase 2: Smooth Motion & Kinematics
*   **Target:** RPi Pico + RPi 4B.
*   **Tasks:**
    *   Implementación de curvas de aceleración (Ease-in/out) para reducir el estrés mecánico en las piezas de **PETG**.
    *   Desarrollo de una API de comunicación serial (UART) entre ambos controladores.
    *   Cálculo de la cinemática del sistema de varillas (mapeo de grados del servo vs. grados reales del tobillo).

### Phase 3: Teleoperation & VR Integration
*   **Target:** RPi 4B + Meta Quest 3S.
*   **Tasks:**
    *   Transmisión de datos de teleoperación mediante **UDP/WebSockets**.
    *   Sincronización del pitch del tobillo con los sensores de movimiento del visor VR.
    *   Monitoreo de telemetría en tiempo real (consumo de corriente y ángulos).

---

## 🛠️ Tech Stack
*   **Languages:** Python 3.x, MicroPython.
*   **Communication:** UART, I2C, WebSockets.
*   **Libraries:** `machine` (Pico), `pyserial`, `numpy` (for kinematics).