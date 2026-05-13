# Engineering Design Log: HEMA Project

## Entry 01: Ankle Joint Design & Rationale
**Date:** May 13, 2026
**Author:** Martin Isla Escudero

### 1. Problem Statement
The ankle joint requires a balance between structural rigidity to support a 1-meter humanoid frame and low inertia to allow rapid stabilization during walking cycles.

### 2. Design Decisions
*   **Pushrod Linkage System:** Instead of mounting the servo directly on the pivot, a linkage system was chosen. 
    *   *Rationale:* This allows the heavy MG995 servo to be mounted higher on the leg, reducing the "unsprung mass" at the foot. This is inspired by high-performance bipedal designs like **Cassie (Agility Robotics)**.
*   **608ZZ Bearing Integration:** The pivot uses standard 608ZZ bearings.
    *   *Rationale:* These are widely available, cost-effective, and designed to handle the radial loads of the robot's weight while providing smooth rotation.
*   **20mm PVC Structural Tubing:** Chosen for the tibia ("bone") section.
    *   *Rationale:* Provides a high strength-to-weight ratio compared to solid 3D printed parts and allows for rapid prototyping of different leg lengths.

### 3. Constraints & Specifications
*   **Degrees of Freedom (DoF):** 1 (Pitch).
*   **Range of Motion (RoM):** ±25° (Total 50°).
*   **Safety Factor:** Designed to withstand 1.5x the estimated static load of the upper assembly.

### 4. Known Issues & Future Iterations
*   **Tolerance Check:** Current CAD shows a 1.3mm gap between the PVC tube and the 3D printed tibia socket. This will be addressed in v5 by implementing a tension-bolt clamp (abrazadera).
*   **Next Step:** Design the servo horn and rocker arm to achieve the 3:1 mechanical advantage.