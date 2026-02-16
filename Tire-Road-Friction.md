# 🛞 Day 10 – Tire–Road Friction | Vehicle Dynamics

After understanding **weight transfer** and **handling balance (understeer & oversteer)**, the next fundamental concept in vehicle dynamics is **tire–road friction**.  
Every force a vehicle generates — braking, acceleration, and cornering — ultimately comes from the interaction between the **tire and the road surface**.

---

## 📘 1. What Is Tire–Road Friction?

Tire–road friction is the force generated at the **contact patch** that resists relative motion between the tire and the road.  
It enables the vehicle to:
- Accelerate  
- Brake  
- Corner  
- Maintain stability  

📌 Without tire–road friction, vehicle control is impossible.

---

## 📘 2. Coefficient of Friction (μ)

The maximum friction force available at a tire is given by:

\[
F = \mu \cdot N
\]

Where:
- \(F\) = friction force  
- \(\mu\) = coefficient of friction  
- \(N\) = normal (vertical) load  

### Typical Coefficient of Friction Values

| Road Surface | μ (Approx.) |
|--------------|------------|
| Dry asphalt  | 0.9 – 1.1  |
| Wet asphalt  | 0.5 – 0.7  |
| Snow         | 0.2 – 0.3  |
| Ice          | 0.05 – 0.1 |

📌 Friction depends on **surface condition and tire properties**, not engine power.

---

## 📘 3. Tire Load Sensitivity

Tires are **load sensitive**:
- Increasing vertical load increases absolute grip  
- Grip does **not increase proportionally** with load  

As a result:
- Two evenly loaded tires generate more total grip  
- Than one heavily loaded tire and one lightly loaded tire  

📌 This explains why **excessive weight transfer reduces total vehicle grip**.

---

## 📘 4. Longitudinal and Lateral Friction

Tires generate friction in two primary directions:

- **Longitudinal friction** → acceleration and braking  
- **Lateral friction** → cornering  

These forces **share the same friction capability** at the contact patch.

---

## 📘 5. Friction Circle (Friction Ellipse Concept)

The friction circle illustrates that:
- A tire has a **limited total friction capacity**
- Longitudinal and lateral forces compete for the same available grip  

Examples:
- Heavy braking reduces cornering capability  
- Hard acceleration reduces steering capability  

📌 Smooth driver inputs allow better utilization of available friction.

---
## 📊 Numerical Examples – Tire–Road Friction

Numerical examples help connect tire–road friction theory with real vehicle behavior.

---

### 🔢 Example 1: Maximum Braking Force on Dry Asphalt

Given:
- Vehicle mass, \( m = 1500 \, \text{kg} \)
- Gravitational acceleration, \( g = 9.81 \, \text{m/s}^2 \)
- Coefficient of friction (dry asphalt), \( \mu = 1.0 \)

Normal load:
\[
N = m \cdot g = 1500 \times 9.81 = 14715 \, \text{N}
\]

Maximum braking force:
\[
F = \mu \cdot N = 1.0 \times 14715 = 14715 \, \text{N}
\]

📌 This is the **maximum force available** to slow the vehicle — braking harder than this will cause wheel slip.

---

### 🔢 Example 2: Effect of Wet Road on Braking

Given:
- Same vehicle
- Wet asphalt friction coefficient, \( \mu = 0.6 \)

\[
F = 0.6 \times 14715 = 8829 \, \text{N}
\]

📌 Available braking force drops by **~40%**, explaining much longer stopping distances on wet roads.

---

### 🔢 Example 3: Tire Load Sensitivity Effect

Assume:
- Total vertical load = 10,000 N

Case 1: Even load distribution  
- Two tires × 5000 N each  
- Total grip ≈ high

Case 2: Uneven load due to weight transfer  
- One tire = 7000 N  
- Other tire = 3000 N  

Because tire friction is **non-linear**, the total grip in Case 2 is **less than Case 1**, even though total load is the same.

📌 This shows why excessive weight transfer reduces overall vehicle grip.

---

### 🔢 Example 4: Friction Circle Limitation

Assume a tire can generate:
- Maximum friction force = 4000 N

If the tire is already using:
- 3000 N for braking

Remaining lateral force:
\[
\sqrt{4000^2 - 3000^2} \approx 2650 \, \text{N}
\]

📌 Heavy braking significantly reduces cornering capability — this is the **friction circle effect**.

---

### 🔢 Example 5: EV Torque and Longitudinal Slip

Given:
- Motor torque at wheel, \( T = 2000 \, \text{Nm} \)
- Tire radius, \( r = 0.3 \, \text{m} \)

Driving force:
\[
F = \frac{T}{r} = \frac{2000}{0.3} \approx 6667 \, \text{N}
\]

If available friction force is lower than this value, **wheel slip occurs**, even at low speeds.

📌 This explains why EVs require aggressive traction and torque control.

---
## 📏 Braking Distance Calculation Using Tire–Road Friction

Braking distance is directly limited by **tire–road friction**, not by brake hardware alone.

### 🔢 Example: Braking Distance on Dry vs Wet Asphalt

Given:
- Vehicle speed, \( v = 100 \, \text{km/h} = 27.78 \, \text{m/s} \)
- Gravitational acceleration, \( g = 9.81 \, \text{m/s}^2 \)

The maximum deceleration achievable is:
\[
a = \mu \cdot g
\]

Braking distance:
\[
s = \frac{v^2}{2a}
\]

---

### Case 1: Dry Asphalt (\( \mu = 1.0 \))

\[
a = 1.0 \times 9.81 = 9.81 \, \text{m/s}^2
\]

\[
s = \frac{27.78^2}{2 \times 9.81} \approx 39.4 \, \text{m}
\]

---

### Case 2: Wet Asphalt (\( \mu = 0.6 \))

\[
a = 0.6 \times 9.81 = 5.89 \, \text{m/s}^2
\]

\[
s = \frac{27.78^2}{2 \times 5.89} \approx 65.5 \, \text{m}
\]

📌 A reduction in friction coefficient from 1.0 to 0.6 increases braking distance by **over 65%**.

---

## 🚗 Real-World Scenario: Highway Emergency Braking While Turning

### Scenario:
You are driving at **100 km/h (27.78 m/s)** on a dry highway (μ = 1.0).  
Suddenly, traffic slows ahead while you are already in a gentle curve.

You must:
- Brake hard  
- Maintain steering to stay in your lane  

This is a **combined braking + cornering** situation.

---

## Step 1: Available Maximum Tire Force

Assume:
- Vertical load per tire = 4000 N  
- μ = 1.0  

Maximum friction force per tire:
\[
F_{max} = \mu \cdot N = 1.0 \times 4000 = 4000 \, N
\]

This is the total force available for BOTH:
- Longitudinal (braking)
- Lateral (cornering)

---

## Step 2: Required Lateral Force for the Curve

Assume curve radius = 200 m

\[
a_y = \frac{v^2}{R}
= \frac{27.78^2}{200}
\approx 3.86 \, m/s^2
\]

Lateral force per tire (simplified):

\[
F_{lat} = m \cdot a_y / 4
\]

For 1500 kg vehicle:

\[
F_{lat,total} = 1500 \times 3.86 = 5790 \, N
\]

Per tire:

\[
F_{lat} \approx 1448 \, N
\]

So each tire is already using:
**~1448 N of its 4000 N friction capacity** for cornering.

---

## Step 3: Remaining Braking Capacity

Using friction circle:

\[
F_{long} = \sqrt{4000^2 - 1448^2}
\approx 3727 \, N
\]

So maximum braking force per tire ≈ 3727 N.

Total braking force:

\[
F_{brake,total} \approx 4 \times 3727
= 14908 \, N
\]

---

## Step 4: Compare to Straight-Line Braking

Straight-line maximum braking:

\[
F_{max,total} = 4 \times 4000 = 16000 \, N
\]

So braking capability reduces from:
- **16000 N → 14908 N**

📌 That is ~7% reduction in braking force just due to cornering.

---

## Engineering Insight

- When braking in a curve, tires must split friction between steering and braking.
- As braking demand increases, lateral capability reduces.
- If braking force exceeds available friction:
  - Front tires saturate first
  - Vehicle understeers
  - Steering becomes ineffective

This explains why:
- Heavy braking mid-corner causes understeer
- ABS activates sooner during turning
- Smooth brake release before turn-in improves stability

---

## Wet Road Version (μ = 0.6)

Now repeat with μ = 0.6:

Maximum per tire:
\[
F_{max} = 0.6 \times 4000 = 2400 \, N
\]

Now:

Lateral force (1448 N) already consumes:
\[
\frac{1448}{2400} \approx 60\%
\]

Remaining braking capacity:

\[
F_{long} = \sqrt{2400^2 - 1448^2}
\approx 1890 \, N
\]

Total braking:

\[
7560 \, N
\]

📌 On wet roads, braking while cornering reduces stopping ability drastically.

---



## ⚙️ ABS Slip-Ratio Example

ABS is designed to keep the tire operating near the **optimal slip ratio**, where braking force is maximized.

### 🔍 Slip Ratio Definition (Braking)

\[
\text{Slip Ratio} = \frac{V - \omega r}{V}
\]

Where:
- \(V\) = vehicle speed  
- \(\omega\) = wheel angular speed  
- \(r\) = tire radius  

---

### 🔢 Example: ABS vs Wheel Lock

Assume:
- Vehicle speed, \( V = 27.78 \, \text{m/s} \)
- Tire radius, \( r = 0.3 \, \text{m} \)

---

### Case 1: Optimal ABS Braking (~15% Slip)

\[
\text{Slip Ratio} = 0.15
\]

The tire operates in the **peak friction region**, generating maximum braking force while maintaining steering control.

📌 ABS modulates brake pressure to remain near this region.

---

### Case 2: Wheel Lock (100% Slip)

\[
\text{Slip Ratio} = 1.0
\]

- Tire slides instead of rolling  
- Friction coefficient drops  
- Steering control is lost  

📌 Locked wheels produce **less braking force** than optimal slip, even though the driver is braking harder.

---
## 🔄 Combined Braking and Cornering – Numerical Example

In real driving, tires rarely experience **pure braking or pure cornering**.  
Most of the time, they must generate **longitudinal and lateral forces simultaneously**.

This behavior is governed by the **friction circle (or friction ellipse)**.

---

### 🔢 Example: Braking While Cornering

Assume:
- Maximum friction force available at a tire = **4000 N**
- Vehicle is braking while turning

---

### Case 1: Straight-Line Braking
- Longitudinal force used = **4000 N**
- Lateral force available = **0 N**

📌 Full braking, no steering capability.

---

### Case 2: Moderate Braking + Cornering
- Longitudinal braking force = **3000 N**

Remaining lateral force:
\[
F_{lat} = \sqrt{4000^2 - 3000^2}
\approx 2650 \, \text{N}
\]

📌 Steering capability is reduced, but still available.

---

### Case 3: Hard Braking + Sharp Turn
- Longitudinal braking force = **3500 N**

\[
F_{lat} = \sqrt{4000^2 - 3500^2}
\approx 1936 \, \text{N}
\]

📌 Limited cornering ability — vehicle tends to understeer.

---

## 🧠 Engineering Insight
- Heavy braking consumes friction capacity  
- Less friction remains for cornering  
- This explains why vehicles understeer when braking hard into a turn  

📌 Smooth brake release before turn-in improves cornering grip.

---

## 📈 Tire Slip vs Friction – Engineering Behavior

Tire friction is a **nonlinear function of slip**, both longitudinally and laterally.

---

### 🔹 Longitudinal Slip vs Friction (Braking)

- Friction increases with slip initially  
- Peaks at **~10–20% slip ratio**  
- Decreases beyond peak (sliding region)

📌 Maximum braking force occurs **before wheel lock**.

---

### 🔹 Lateral Slip Angle vs Friction (Cornering)

- Lateral force increases with slip angle  
- Peaks at **small slip angles (≈ 6–10° for road tires)**  
- Drops as tire slides

📌 Maximum cornering force occurs **before visible sliding**.

---

## 📊 Typical Slip–Friction Curves (Conceptual)

### Longitudinal (ABS Relevance)

 

## 📘 6. Slip Ratio and Slip Angle

### A. Slip Ratio (Longitudinal Slip)

Slip ratio occurs when wheel speed differs from vehicle speed:
- During braking → wheel speed is lower  
- During acceleration → wheel speed is higher  

Maximum braking force occurs at **small slip ratios**, not at full wheel lock.

---

### B. Slip Angle (Lateral Slip)

Slip angle is the angle between:
- Wheel heading direction  
- Actual direction of travel  

Key behavior:
- Small slip angles → linear force buildup  
- Large slip angles → saturation and loss of grip  

📌 Peak lateral force occurs **before visible sliding**.

---

## 📘 7. Influence of Road and Environmental Conditions

Tire–road friction is strongly affected by:
- Water (wet roads, hydroplaning)  
- Temperature  
- Surface roughness  
- Contaminants (dust, oil, debris)  

This explains:
- Increased braking distance on wet roads  
- Reduced grip with cold tires  
- Tire warm-up requirements in motorsport  

---

## 📘 8. Tire–Road Friction and Vehicle Control Systems

### Anti-lock Braking System (ABS)
- Prevents wheel lock  
- Maintains optimal slip ratio  

### Traction Control System (TCS)
- Limits wheel spin  
- Keeps tires within high-friction region  

### Electronic Stability Control (ESC)
- Controls yaw using selective braking  
- Fully dependent on available tire friction  

📌 These systems **manage friction — they do not create it**.

---

## 📘 9. Motorsport Perspective

In motorsport:
- Tires operate near peak friction levels  
- Smooth steering, braking, and throttle inputs are critical  
- Excessive sliding overheats tires and reduces grip  

📌 Fast lap times come from **maximizing usable friction**, not exceeding it.

---

## 📘 10. EV-Specific Tire–Road Friction Effects

Electric vehicles introduce unique challenges:
- High vehicle mass  
- Instant torque delivery  
- Strong regenerative braking  

Effects include:
- Higher risk of longitudinal slip  
- Rear axle instability during regenerative braking  
- Increased reliance on torque and brake control software  

📌 In EVs, friction management is a **combined hardware and software problem**.

---

## 🏁 Trail Braking – Practical Use of Tire–Road Friction

**Trail braking** is a driving and vehicle dynamics concept where the driver **gradually releases brake pressure while entering a corner**, instead of completing all braking in a straight line.

From an engineering perspective, trail braking is about **managing how longitudinal and lateral tire forces share available friction**.

---

## 🔍 Why Trail Braking Works

When braking in a straight line:
- Most of the tire’s friction capacity is used for **longitudinal force**
- Lateral force capability is minimal

As the driver begins turn-in:
- Brake pressure is reduced  
- Longitudinal force demand decreases  
- More friction becomes available for **lateral force**

📌 This smooth transition keeps the tire operating **near the peak of the friction circle**.

---

## 🔄 Trail Braking and Weight Transfer

Trail braking also affects **load transfer**:

- Braking shifts load to the **front axle**
- Increased front load improves front tire grip
- Gradual brake release prevents sudden rear unloading

This helps:
- Reduce entry understeer  
- Improve front-end response  
- Maintain rear stability  

📌 Abrupt brake release can cause rear instability or snap oversteer.

---

## 📐 Trail Braking vs Early Brake Release

### Early Brake Release
- Braking completed before turn-in  
- Sudden transfer to lateral forces  
- Higher risk of understeer at corner entry  

### Trail Braking
- Brake force reduced progressively  
- Smooth force blending  
- Improved rotation and corner entry grip  

---

## 🏎️ Motorsport Perspective

In motorsport:
- Trail braking is used to fine-tune **corner entry rotation**
- Small brake inputs help rotate the car toward the apex
- Excessive trail braking can overload front tires and destabilize the rear

📌 Effective trail braking is **vehicle- and setup-dependent**.

---

## ⚡ EV Considerations in Trail Braking

In EVs:
- Regenerative braking often acts on specific axles
- Rear-biased regen can increase entry oversteer
- Front-biased regen may increase understeer

📌 EV trail braking requires **careful coordination between regen and friction brakes**.

---

## 🧠 Insight

Trail braking is not about braking later —  
it is about **how braking force is released**.

Proper trail braking:
- Maximizes friction usage  
- Improves corner entry balance  
- Reduces understeer  
- Maintains stability  

📌 It is a practical demonstration of **tire–road friction management**.

---


## 💻 Mini MATLAB Example – Tire Friction Modeling

To better understand tire–road friction behavior, we can visualize:

1. The **friction circle**
2. The **slip ratio vs friction curve**

Below is a simple MATLAB script for demonstration.

---

### 📌 1. Friction Circle Visualization

matlab
clc; clear; close all;

% Parameters
mu = 1.0;           % Coefficient of friction (dry road)
N = 4000;           % Normal load per tire (N)
Fmax = mu * N;      % Maximum friction force

% Create circle
theta = linspace(0, 2*pi, 1000);
Fx = Fmax * cos(theta);
Fy = Fmax * sin(theta);

figure;
plot(Fx, Fy, 'LineWidth', 2);
grid on;
axis equal;
xlabel('Longitudinal Force (N)');
ylabel('Lateral Force (N)');
title('Tire Friction Circle');
clc; clear; close all;

### 📌 2. Slip ratio range
slip = linspace(0, 1, 100);

% Simple tire model (qualitative)
mu_peak = 1.0;
slip_peak = 0.15;

mu = mu_peak * (slip ./ slip_peak) .* exp(1 - slip ./ slip_peak);

figure;
plot(slip, mu, 'LineWidth', 2);
grid on;
xlabel('Slip Ratio');
ylabel('Friction Coefficient');
title('Slip Ratio vs Friction');




## 🧠 Key Takeaways

- Tire–road friction limits all vehicle performance  
- Friction depends on surface condition and tire properties  
- Tires are load sensitive  
- Longitudinal and lateral forces compete for grip  
- Smooth control inputs maximize available friction
- Braking and steering share the same friction limit.
- The higher the speed, the greater the friction demand.
- Wet roads dramatically reduce safety margin.
- Combined braking + cornering increases understeer risk.
- Smooth control inputs preserve friction reserve.

This is why highway emergency maneuvers are so sensitive to road conditions.


---

## 🧠 Engineering Insight

- Maximum grip is limited by tire–road friction, not engine or motor power  
- Uneven loading reduces total grip due to tire load sensitivity  
- Braking, steering, and acceleration must share available friction  
- EV torque must be carefully managed to stay within friction limits 
- Maximum braking force occurs at **partial slip**, not full lock  
- ABS does not shorten braking distance in all cases, but it:
  - Maintains steerability  
  - Prevents instability  
  - Keeps tires near peak friction
  - Even with the same brakes and driver input, braking distance increases significantly as tire–road friction decreases. This is why road condition awareness is critical for safety.

---

## 📌 Practical Takeaway

Braking performance depends on:
- Tire–road friction  
- Slip control (ABS)  
- Load distribution during braking  

📌 Modern braking systems manage **available friction**, they do not create it.
---

## 🚀 Next Topic – Day 11
**Brake Force Distribution & Braking Stability**
