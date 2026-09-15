# naval-structural-fea-postgrad-thesis

# Finite Element Analysis (FEA) of a Bulk Carrier Midship Section

This repository contains my postgraduate specialization project (Specialization Thesis) completed at **ESSS (Engineering Simulation and Scientific Software)**.

The project evaluates the longitudinal stresses on the midship section (parallel middle body) of the **China Steel Liberty** bulk carrier using the Finite Element Method (FEM) in Ansys, comparing the numerical results with analytical classic beam theory (Ship Beam Theory).

---

## Technical Scope & Key Contributions

- **Geometry & CAD Modeling**: Modeled the midship structural section (plating and longitudinal stiffeners) in **Ansys SpaceClaim** based on *Significant Ships (2019)* data and IACS (International Association of Classification Societies) Common Structural Rules.
- **Stiffener Profiles Integration**: Applied commercial **Bulb Flat profiles** (HP 380x14, HP 300x12, and HP 320x12) modeled as line bodies with realistic section properties for deck, side, and bottom structures.
- **Finite Element Modeling & Meshing**: 
  - Utilized **SHELL181** shell elements with 6 degrees of freedom per node and quadratic displacement interpolation.
  - Applied stress-concentration mitigation techniques, including edge rounding (fillets) and localized mesh refinement (Face Sizing, Adaptive Sizing, and mesh convergence study at 28,727 nodes).
- **Boundary Conditions & IACS Wave Loads**:
  - Modeled **Remote Points** at fore and aft boundaries with rigid behavior to apply pure bending moments.
  - Calculated wave vertical bending moments for extreme sea conditions based on **IACS Common Structural Rules for Bulk Carriers**, evaluating both **Hogging** ($12.72 \times 10^6 \text{ kNm}$) and **Sagging** ($-12.08 \times 10^6 \text{ kNm}$) load cases.
- **Non-Linear FEA Simulation**: Configured the non-linear solver with **Large Deflection ON** and custom substep controls to resolve contact behavior (bonded welds) and geometry update iterations.
- **Analytical Comparison & Benchmarking**: Computed section modulus and moments of inertia using the Parallel Axis Theorem, comparing FEA normal stress distribution against classical **Ship Beam Theory** ($\sigma = \frac{M y}{I}$).

---

## Tools & Software Used

- **FEA Solver & Pre-processor**: Ansys Mechanical / Ansys Workbench
- **3D CAD & Geometry Handling**: Ansys SpaceClaim
- **Governing Standards**: IACS Common Structural Rules for Bulk Carriers and Oil Tankers

---

## Author

- **Eng. Gustavo Miranda dos Santos**[cite: 1, 2]
  - Postgraduate Specialization in Numerical Simulation / FEA — ESSS[cite: 1, 2]
