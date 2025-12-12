# 🚗 Traction Force vs Resistive Forces – Vehicle Dynamics

Vehicle longitudinal motion is governed by the fundamental force balance:

\[
F_{net} = F_{traction} - F_{resistive}
\]

Where:
- F_{net} = net force acting on the vehicle  
- F_{traction} = driving force generated at the wheels  
-  F_{resistive} = sum of all forces opposing motion  

If \(F_{net} > 0\), the vehicle accelerates.  
If \(F_{net} = 0\), it maintains speed.  
If \(F_{net} < 0\), it decelerates.

The magnitude and sign of \(F_{net}\) determine whether a vehicle **accelerates**, **maintains speed**, or **decelerates**.

---

## 📘 1. Traction Force

Traction force is the usable driving force transmitted at the tire–road interface. It is generated from engine/motor torque through the drivetrain.

\[
F_{traction} = \frac{T_{w}}{r}
\]

### Variables:
| Symbol | Meaning |
|--------|---------|
|\(T_{w}\): Wheel torque | Torque delivered at the wheels (after gear reduction) |
| - \(r\): Tire radius  | Effective tire radius (m) |

A higher torque or smaller tire radius increases traction force.

---

### 🔹 Maximum Available Traction (Friction Limit)


\[
F_{max} = \mu N
\]

Variables:  
- \(\mu\): Friction coefficient  
- \(N\): Normal load 

Where:
| Symbol | Meaning |
|--------|---------|
| \(\mu\) | Tire–road friction coefficient |
| \(N\) | Normal force acting on driven wheels |

If \(F_{max} = \mu N\), tire slip occurs.

---

## 📘 2. Resistive Forces

Total resistance opposing motion is:

\[
F_{resistive} = F_{rr} + F_{d} + F_{g}
\]

These forces reduce acceleration and increase energy consumption.

---

## **A. Rolling Resistance**

\[
F_{rr} = C_{rr} \, m \, g
\]

### Variables:
| Symbol | Meaning |
|--------|---------|
| \(C_{rr}\) | Rolling resistance coefficient |
| \(m\) | Vehicle mass (kg) |
| \(g\) | Gravity (9.81 m/s²) |

Rolling resistance dominates at low speeds.

---

## **B. Aerodynamic Drag**

\[
F_d = \frac{1}{2} \rho C_d A v^2
\]

### Variables:
| Symbol | Meaning |
|--------|---------|
| \(\rho\) | Air density (1.225 kg/m³) |
| \(C_d\) | Drag coefficient |
| \(A\) | Frontal area (m²) |
| \(v\) | Vehicle speed (m/s) |

Drag increases with the square of speed and dominates at high speeds.

---

## **C. Gradient Force**

Angle form:

\[
F_g = m g \sin\theta
\]

Grade (%) form:

\[
F_g = m g \left(\frac{G}{100}\right)
\]

### Variables:
| Symbol | Meaning |
|--------|---------|
| \(m\) | Vehicle mass (kg) |
| \(g\) | Gravitational acceleration |
| \(\theta\) | Road incline angle (radians) |
| \(G\) | Grade percentage (%) |

Gradient force dominates during hill climbing.

---

# 📘 3. Combined Resistive Force

\[
F_{resistive}
= C_{rr} m g
+ \frac{1}{2} \rho C_{d} A v^{2}
+ m g \left( \frac{G}{100} \right)
\]

Each term dominates under different conditions:
- Low speed → rolling + gradient  
- High speed → aerodynamic drag  

---

# 📘 4. Vehicle Acceleration Condition

\[
F_{net} = F_{traction} - F_{resistive}
\]

\[
a = \frac{F_{net}}{m}
\]

Where:
- \(a\) = acceleration (m/s²)

### Vehicle states:
- \(F_{traction} > F_{resistive}\) → acceleration  
- \(F_{traction} = F_{resistive}\) → constant speed  
- \(F_{traction} < F_{resistive}}\) → deceleration  

---

# 📊 5. Real-World Example (With Variable Explanation)

Vehicle parameters:
- \(m = 1600 \, \text{kg}\)  
- \(v = 80 \, \text{km/h} = 22.22 \, \text{m/s}\)  
- \(C_{rr} = 0.012\)  
- \(C_d = 0.30\)  
- \(A = 2.2 \, \text{m}^2\)  
- \(\rho = 1.225\)  
- \(G = 0\%\)

---

### Step 1 — Rolling Resistance

\[
F_{rr} = 0.012 \cdot 1600 \cdot 9.81 = 188.3 \, \text{N}
\]

---

### Step 2 — Aerodynamic Drag

\[
F_d = \frac{1}{2} \cdot 1.225 \cdot 0.30 \cdot 2.2 \cdot (22.22)^2
\]

\[
F_d \approx 199 \, \text{N}
\]

---

### Step 3 — Gradient Force

\[
F_g = 0
\]

---

### Step 4 — Total Resistive Force

\[
F_(resistive) = 188.3 + 199 = 387.3 \, 
\]

---

### Step 5 — Assume Traction Force

\[
F_(traction} = 500 \, 
\]

---

### Step 6 — Net Force

\[
F_{net} = 500 - 387.3 = 112.7 \, \text{N}
\]

---

### Step 7 — Acceleration

\[
a = \frac{112.7}{1600} = 0.0704 \, {m/s}^2
\]

Vehicle **accelerates**, but slowly due to high resistive forces.

---

# 🔋 6. Engineering Importance

### EV:
- Higher resistive forces → increased battery current  
- Drag and gradient significantly reduce range  
- Motor heating increases with \(F_{\text{traction}}\) demand  

### ICE:
- Higher resistances → gear downshifts  
- Increased fuel consumption  
- Reduced acceleration capability  

### Simulation Uses:
- WLTP/FTP road-load modeling  
- Powertrain sizing  
- EV range estimation  
- Gradeability tests  
- Acceleration modeling  

---

# ⭐ 7. Summary (5 Key Points)

- Traction force originates from wheel torque and tire radius.  
- Resistive forces include rolling, drag, and gradient components.  
- Net force determines acceleration.  
- Drag dominates high-speed driving; gradient dominates climbs.  
- Essential for EV range, ICE fuel efficiency, and vehicle simulation.

---

# 🚀 Next Articles

- Road-Load Coefficients (f₀, f₁, f₂)  
- Acceleration Modeling  
- Tire Dynamics & Slip  

