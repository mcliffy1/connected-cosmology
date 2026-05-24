# SVT & NLS Dynamics Simulator (v5.5)

A high-fidelity, real-time interactive canvas visualizer designed to model cosmological and quantum configurations through the lens of **Superfluid Vacuum Theory (SVT)** and the **Nonlinear Schrödinger / Gross-Pitaevskii Equation (GPE)**.

This simulator bridges the gap between abstract fluid mechanics and structural physical emergence, demonstrating how localized matter envelopes ("solitons") condense stably out of a non-linear superfluid medium.

---

## 🚀 Key Accomplishments & Refinements

* **Defensive DOM Architecture:** Eliminated critical top-down asynchronous race conditions by encapsulating layout engine mapping and UI binding securely inside the `window.onload` lifecycle hook.
* **Gross-Pitaevskii Mathematical Mapping:** Transitioned the core rendering engine from abstract visual aesthetics to a rigorous scientific framework, explicitly mapping interactive variables directly to the field nonlinearity term $\frac{\lambda}{2}|\psi|^4$.
* **Lineweaver Stability Corridor Coupling:** Implemented a targeted structural preset button that dynamically calculates and restricts the fluid mass ($M_{\text{eff}}$) and self-interaction ($\lambda$) coefficients to the precise "stable condensation windows" highlighted in cosmic phase space literature.
* **Dynamic Phase Space Visualization:** Engineered an interactive, shifting "Forbidden Bounds" matrix overlay. Rather than functioning as a static watermark, the geometric intersections automatically adapt to slider inputs, visually mapping out the changing margins between the **Schwarzschild Boundary** (General Relativity) and the **Compton Wavelength Boundary** (Quantum Mechanics).

---

## 🌌 Scale Domains Mode Matrix

The simulation engine features four core scaling thresholds, each mapping specific fluid parameter profiles to emergent macro and micro structures:

| Domain Mode | Theoretical Paradigm | Applied Visual Mechanics |
| --- | --- | --- |
| **Galactic Soliton** | Bose-Einstein Condensate (BEC) Dark Matter | Models flat velocity curves and stationary breather spiral arms, completely bypassing the classical galactic wind-up paradox. |
| **White's Atom** | Acoustic Bound States & Evanescent Stop-Bands | Simulates hydrogen orbital constraints via temporal dispersion ($\omega = Dq^2$). Boundary exclusion acts as a hydrodynamic analog to the Pauli Exclusion Principle. |
| **Couder Pilot-Wave** | Non-Local Cavity Entanglement | Hydrodynamic analog to quantum non-locality based on Yves Couder's walking droplet experiments. Shifts to a single node instantaneously modulate shared boundary conditions. |
| **Vortex Core** | Non-Singular Superfluid Vacuum | Splits the workspace canvas to contrast general relativity's unphysical infinite singularity breakdown against the self-limiting, localized vortex core of the NLS framework. |

---

## 🛠️ Variable Parameter Mapping

```
     [Slider Controls]                      [Gross-Pitaevskii Field Engine]
Non-Linear Self-Interaction (λ) --------> Regulates Merle field expansion vs. collapse
Effective Fluid Mass (M_eff)    --------> Dictates Madelung bulk fluid velocity profile
Temporal Dispersion (D)         --------> Enforces spatial boundaries & reactive stop-bands
Global Phase State (θ)          --------> Drives wave direction, velocity scales, & vectors

```

* **Non-Linear Interaction ($\lambda$):** Directly corresponds to Frank Merle's non-linear field self-interaction index. It acts as an adjustable counter-pressure, halting blow-ups and ensuring localized envelope permanence.
* **Effective Mass ($M_{\text{eff}}$):** Governs the velocity fields of the background plenum fluid medium, scaling the stochastic damping and phase-mixing intensities.
* **Temporal Dispersion ($D$):** Maps to Dr. Harold White's spatial boundary conditions, forcing natural quantization into discrete orbital envelopes without requiring probability assumptions.
* **Global Phase State ($\theta$):** Sweeps configuration space alignments. Setting this parameter to $1.00\pi$ triggers an absolute anti-phase vector inversion, simulating superluminal topological vortex transitions.

---

## 📐 The Physics of the Forbidden Bounds

When toggled, the simulator draws the boundaries of physical existence derived from log-log mass-radius limits:

---

## code Structure & Implementation

The application is deployed entirely within a zero-dependency, unified single-file architecture (`index.html`) using raw HTML5 Canvas and native strict-block ES6+ JavaScript.

### File Geometry

* **CSS Layout:** Implements a strict flexbox-split UI sidebar dashboard housing alongside a fully responsive canvas container, fitted with CSS media breakpoints to suppress graphic rendering on small viewports safely.
* **State Registry:** Houses an isolated, mutable configuration state cache (`state`) sampled 60 times per second by the animation frame execution cycle.
* **Error-Insulated Lifecycle:** Element nodes are securely cached via element presence checks before handler hooks are allocated, rendering the application highly resilient against front-end rendering drops.
