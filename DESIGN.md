✅ Step 1: Feasibility Validation

This stage is all about proving that your idea is physically and practically achievable.

1.1 Define Core Specs (with ultralight in mind)
	•	Max empty weight: ≤ 254 lbs (per FAA Part 103)
	•	Cruise speed: ≤ 55 knots (~63 mph)
	•	Stall speed: ≤ 24 knots
	•	Fuel capacity: ≤ 5 gallons (if using liquid fuel)
	•	Single occupant, no certification required

1.2 Basic Mission Profile Assumptions
	•	VTOL at takeoff and landing, but transitions to efficient fixed-wing flight
	•	Hybrid powertrain: microturbine + electric
	•	Cruise range target: ~100–300 km (depending on battery and fuel energy density)

1.3 Use Back-of-Envelope Physics
	•	Thrust-to-weight ratio ≥ 1.2 for VTOL
	•	Wing loading for stable fixed-wing flight (~8–10 lb/ft² is a good ultralight range)
	•	Energy balance:
	•	Battery: ~200 Wh/kg
	•	Jet-A fuel (microturbine): ~12,000 Wh/kg equivalent
	•	Power requirement: ~60–80 hp (for brief hover), ~15–25 hp (cruise)
	•	Rotor disk loading & prop efficiency need to be modeled for multirotor hover vs. forward flight

⸻

✅ Step 2: Design Process

2.1 Conceptual Design
	•	Choose configuration: Lift + Cruise or Tilting rotors
	•	Prioritize simplicity: fixed-wing + dedicated lift props avoids mechanical tilt
	•	Use known configurations like:
	•	Joby S4 (tilt rotor)
	•	Opener Blackfly (fixed-tilt)
	•	Lilium Jet (ducted fan array)

2.2 Modeling & Simulation

Tools to use:
	•	XFLR5 or AVL for aerodynamic modeling (fixed-wing)
	•	OpenVSP or SolidWorks + Flow Simulation for conceptual 3D airflow
	•	eCalc, QGroundControl, or Rotorcraft CFD tools for rotor performance
	•	Simple Excel/Google Sheets to model mass/power trade-offs

Things to Model:
	•	Required power to hover vs cruise
	•	Flight time vs fuel/battery energy
	•	Structural loading and CG during all phases of flight
	•	Redundancy tolerance (safe landing if 1–2 rotors fail?)

⸻

✅ Step 3: Prototyping on a Budget

3.1 Scale RC Prototyping
	•	Start with 1/4–1/3 scale to test configuration, aerodynamics, and flight control
	•	Use Pixhawk or CubePilot for VTOL/autonomous controls
	•	Use 3D printing + foam/fiberglass for low-cost iteration
	•	Test transitions from hover to cruise

3.2 Subsystems Testing
	•	Build/test the hybrid-electric powertrain separately (turbine + generator + battery + ESC)
	•	Monitor thermal management of turbine and electrical systems

⸻

✅ Step 4: Full-Scale Testbed
	•	Build with composite (foam sandwich, fiberglass, carbon) for strength-to-weight
	•	Start tethered hover tests first (even indoors if needed)
	•	Integrate controls with safety overrides and logging

⸻

✅ Step 5: Principles to Master

✈ Aerodynamics
	•	Lift/drag ratio for cruise
	•	Disk loading for hover efficiency
	•	Wing aspect ratio and airfoil choice

⚡ Energy & Power
	•	Battery Wh/kg vs fuel Wh/kg
	•	Motor/ESC sizing for surge power
	•	Efficiency curves of propellers vs thrust

🔁 Redundancy
	•	How many rotors are needed to survive one rotor failure?
	•	Independent ESCs and power buses for critical systems

🧠 Control Systems
	•	PID + attitude control for hover
	•	Transition logic (quadcopter to plane)
	•	GPS and barometer stabilization

⸻

✅ Key Ratios & Rules of Thumb

Principle	Guideline
Thrust-to-weight (VTOL)	≥ 1.2–1.3
Wing loading (cruise)	~8–10 lb/ft²
Disk loading (hover)	< 10 lb/ft² for efficiency
Battery energy density	~200 Wh/kg (Li-ion)
Jet-A energy density	~12,000 Wh/kg equivalent
Rotor efficiency	3–5 lb of thrust per kW (multirotor baseline)
Endurance improvement (hybrid)	2x–4x vs battery-only with small turbine generators


⸻

✅ Development Path (Simplified)

| Phase | Goal | Tools |
|-------|------|-------|
| 1 | Define specs, sketch concepts | Pen & paper, spreadsheets |
| 2 | Run energy and weight feasibility | Excel, CAD, basic CFD |
| 3 | Build RC prototypes | 3D printing, Pixhawk, ArduPilot |
| 4 | Ground-test hybrid system | Bench rig, multimeter, logging |
| 5 | Build subscale VTOL/crosswind models | Foam core + composite skin |
| 6 | Full-scale flight testing | Composite structure, GPS, IMU |

⸻
