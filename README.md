# Antariksh-1 CanSat — Descent Simulation

**Team Antariksh-1** · SEVA FIRST Innovation Challenge 2026 · **NAT-004** (Industry & Government track)
Screen-2 supporting evidence — Point 4 (calculations & simulation).

## What this is
A physics simulation of a CanSat descending under a parachute after release from a drone at 500 m,
together with the horizontal landing drift for a range of wind speeds.

## Model
Vertical motion: `m·dv/dt = m·g − ½·ρ·Cd·A·v²`, integrated at `dt = 1 ms`.

| Parameter | Value |
| --- | --- |
| Payload mass `m` | 0.6 kg (within the ≤ 700 g limit) |
| Parachute canopy area `A` | 0.334 m² (≈ 65 cm diameter) |
| Drag coefficient `Cd` | 0.8 |
| Air density `ρ` | 1.225 kg/m³ |
| Gravity `g` | 9.81 m/s² |

## Results
- **Terminal descent velocity: 6.00 m/s** (target band 5–8 m/s — inside)
- **Descent time from 500 m: 83.8 s**
- **Landing drift:** 236 m at 3 m/s wind; 402 m at 5 m/s wind

The drift result shows why landing accuracy is the hardest requirement and why a passive
parachute alone cannot guarantee the recovery zone.

## Files
- `cansat_descent_sim.py` — the simulation
- `descent_sim.png` — altitude & descent-rate vs time; drift vs wind
- `Antariksh-1_Descent_Simulation_Report.pdf` — evidence report

## Run
```
pip install numpy matplotlib
python cansat_descent_sim.py
```

*Assumptions are indicative (constant air density) and results are confirmed by drop testing during VALIDATE.*
