# Engineering Design Log: HEMA Project

## Entry 01: Ankle Joint v4 Review
**Date:** May 13, 2026
**Author:** Martin Isla Escudero
**Subsystem:** Mechanical / Ankle
**Status:** In review

### 1. Objective
Define a mechanically compact ankle joint for a 1 m humanoid frame while keeping the distal mass as low as possible.

### 2. Engineering context
The current concept uses a pushrod linkage to move the MG995 away from the foot and a pair of 608ZZ bearings to support the rotary joint. The tibia prototype is based on 20 mm PVC tubing combined with 3D printed interfaces.

### 3. Design decisions
* **Pushrod linkage:** selected to reduce unsprung mass at the foot and keep the servo higher in the leg.
    * Rationale: lower inertia at the distal end improves dynamic response and reduces the torque penalty during leg motion.
* **608ZZ bearings:** selected as the primary pivot support.
    * Rationale: standard, low-cost, easy to source, and adequate for the radial loads expected in this prototype stage.
* **20 mm PVC structural tube:** selected as the tibia core during prototyping.
    * Rationale: fast to source, simple to machine, and sufficient for early fit-checks before moving to a more optimized structural solution.

### 4. Constraints and target values
* **Degrees of freedom:** 1 axis, pitch.
* **Range of motion:** +/-25 degrees.
* **Target safety factor:** 1.5x the estimated static load of the upper assembly.
* **Assembly goal:** no forced fit that requires uncontrolled sanding or ad hoc reshaping during assembly.

### 5. Open technical issues
* **PVC-to-socket fit:** current CAD indicates a 1.3 mm gap between the PVC tube and the 3D printed tibia socket.
* **Retention strategy:** the joint still needs a final decision between clamp-style retention, interference fit, or a hybrid solution.
* **Torque path:** the servo horn and rocker geometry still need to be finalized to confirm the 3:1 mechanical advantage.

### 6. Validation plan
* Verify the actual clearance between printed parts and the PVC tube after export.
* Check whether the clamp can absorb print variation without over-stressing the socket.
* Confirm that the linkage does not collide through the full +/-25 degree travel.
* Estimate the available torque margin at the worst-case ankle position.

### 7. Next iteration
Prepare the servo horn and rocker arm geometry, then close the retention concept for the PVC tube before moving to a new prototype export.