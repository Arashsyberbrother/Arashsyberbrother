<div align="center">

<!-- Academic Header Banner -->
<img src="./assets/banner.png" width="100%" alt="Arash Mohammadrezaei - Computational Nuclear Engineering & Scientific Computing" />

<br/><br/>

# Arash Mohammadrezaei
### **Computational Nuclear Engineering & Scientific Computing**
**B.Sc. in Nuclear Engineering** • *Reactor Physics • Stiff Numerical Methods • Scientific Machine Learning*

[![Status: Seeking Graduate Opportunities](https://img.shields.io/badge/Status-Seeking%20M.Sc.%20%2F%20Ph.D.%20Opportunities-0ea5e9?style=for-the-badge&logo=googlescholar&logoColor=white)](mailto:arashrezaii28@gmail.com)
[![Direct Email](https://img.shields.io/badge/Email-arashrezaii28%40gmail.com-ea4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:arashrezaii28@gmail.com)
[![GitHub Profile](https://img.shields.io/badge/GitHub-Arashsyberbrother-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Arashsyberbrother)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Arash%20Mohammadrezaei-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com)

</div>

---

## 🔬 Academic Profile & Research Positioning

I am an undergraduate researcher in **Nuclear Engineering** specializing in **computational reactor physics, stiff numerical time-integration, and scientific machine learning (SciML)**. 

My work focuses on developing transparent, mathematically verified computational frameworks for physical and nuclear systems—bridging classical reactor physics theory (eigenvalue diffusion and point kinetics) with modern numerical analysis (implicit stiff solvers, order-of-accuracy verification) and scientific machine learning (physics-informed neural networks).

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                        COMPUTATIONAL RESEARCH PORTFOLIO ARC                            │
└────────────────────────────────────────────────────────────────────────────────────────┘
  Project 1: Physics-Informed Neural Network Lab (Numerical & SciML Foundations)
             └─ 1D transient heat equation, autograd vs. Crank-Nicolson FDM,
                A-stability and non-L-stability analysis, empirical error norms
                                           │
                                           ▼
  Project 2: 1D Neutron Diffusion Reactor Simulator (Steady-State Spatial Neutronics)
             └─ One-group diffusion eigenvalue problem, conservative FDM, Thomas TDMA,
                power iteration, heterogeneous core-reflector physics, reflector savings
                                           │
                                           ▼
  Project 3: Reactor Point Kinetics & Transient Analysis (Time-Dependent Dynamics)
             └─ 7-ODE PRKE, 6-group delayed precursors (Keepin U-235), bordered Jacobian,
                stiff implicit solvers (BDF2, CN, Euler), exact Inhour analytical benchmark,
                Prompt Jump Approximation asymptotic verification
                                           │
                                           ▼
  Future:    Scientific Machine Learning for Coupled Reactor Dynamics
             └─ Neural ODEs and operator learning for stiff, multi-scale transient physics
```

---

## 🏆 Featured Research Repositories

### 1. [Reactor Point Kinetics & Transient Analysis](https://github.com/Arashsyberbrother/reactor-point-kinetics-transient-analysis)
*Time-Dependent Reactor Kinetics with 6 Delayed-Neutron Groups & Stiff Implicit Solvers*

- **Problem:** Integrating the stiff 7-ODE Point Reactor Kinetics Equations (PRKE) across disparity in time constants from prompt neutron lifetime ($\Lambda = 50\,\mu\text{s}$) to precursor half-lives ($T_{1/2} \approx 55.7\text{ s}$).
- **Numerical Formulation:** Developed custom vector-matrix implicit solvers (BDF2, Crank-Nicolson, Backward Euler) with exact bordered-diagonal Jacobian $\mathbf{A}(t)$, alongside an adaptive 5th-order Radau IIA reference solver.
- **Verification Standard:** Derived the exact 7-pole Inhour characteristic equation and Cauchy residue amplitude expansion ($\sum A_j = 1.0$) as a closed-form analytical benchmark for step reactivity insertions.
- **Key Verified Findings:**
  - Critical equilibrium null-transient preserved over $1000\text{ s}$ ($20,000$ steps) with relative drift $\le 3.95 \times 10^{-14}$.
  - Verified theoretical order of accuracy ($p = 0.983$ Euler, $p = 2.000$ CN, $p = 1.976$ BDF2).
  - Evaluated Prompt Jump Approximation as an asymptotic singular perturbation limit ($0.25\%$ discrepancy at $+0.20\$$).
  - Characterized prompt-supercritical excursion ($+1.05\$$) with prompt timescale $\tau_{\text{prompt}} \approx 154\text{ ms}$.
- **Tests & Quality:** 55 / 55 automated tests passing; comprehensive publication figures and CSV tables.

---

### 2. [1D Neutron Diffusion Reactor Simulator](https://github.com/Arashsyberbrother/neutron-diffusion-reactor-simulator)
*Steady-State Reactor Physics, Finite-Difference Discretization & Reflector Savings*

- **Problem:** Solving the steady-state, one-group neutron diffusion eigenvalue problem to determine core criticality ($k_{\text{eff}}$), spatial scalar flux ($\phi(x)$), and fission power ($P(x)$) for bare and reflected cores.
- **Numerical Formulation:** Conservative cell-centered second-order finite difference discretization, harmonic mean interface diffusion coefficients, $\mathcal{O}(N)$ Thomas algorithm (TDMA), and power iteration.
- **Verification Standard:** Exact analytical fundamental mode buckling benchmark for bare homogeneous slab ($k_{\text{eff}} = \nu\Sigma_f / (\Sigma_a + D B_g^2)$).
- **Key Verified Findings:**
  - Analytical benchmark agreement to within $0.44\text{ pcm}$ error ($|k_{\text{eff}} - k_{\text{exact}}| = 4.41 \times 10^{-6}$).
  - Confirmed asymptotic spatial quadratic convergence ($p = 2.000, R^2 = 1.0000$) across $N \in [20, 640]$ grid cells.
  - Demonstrated $+4641.1\text{ pcm}$ reactivity gain from reflector back-scattering and $22.0\%$ core power flattening.
  - Solved critical fuel thickness ($T_{\text{crit}} = 24.9658\text{ cm}$) with residual $|k_{\text{eff}} - 1.0| = 0.13\text{ pcm}$.
- **Tests & Quality:** 45 / 45 automated tests passing; 12 publication figures.

---

### 3. [Physics-Informed Neural Network Lab](https://github.com/Arashsyberbrother/physics-informed-neural-network-lab)
*Scientific Machine Learning Foundations & Classical Crank-Nicolson Numerical Benchmarks*

- **Problem:** Evaluating the fidelity, convergence, and computational trade-offs of Physics-Informed Neural Networks (PINNs) against exact analytical solutions and classical finite-difference methods for the 1D transient heat equation.
- **Methodology:** Fully connected PyTorch MLP with hyperbolic tangent activations, Latin Hypercube spatio-temporal sampling, autograd differential PDE residuals, and an implicit 2nd-order Crank-Nicolson numerical baseline.
- **Numerical & Rigor Insights:**
  - Demonstrated why Crank-Nicolson is A-stable but strictly non-L-stable ($|R(-\infty)| = 1$), highlighting the mesh ratio monotonicity condition ($r = \alpha \Delta t / \Delta x^2 \le 1$).
  - Evaluated PINN error fields ($L_\infty = 9.03 \times 10^{-3}$, relative $L_2 = 0.91\%$) against classical FDM ($L_\infty = 1.75 \times 10^{-5}$).
  - Articulated the computational boundary: classical FDM solves in $\sim 18\text{ ms}$ vs. $\sim 265\text{ s}$ for PINN optimization on CPU, establishing when SciML is—and is not—appropriate.
- **Tests & Quality:** 19 / 19 automated tests passing; automated convergence and checkpointing pipelines.

---

## 🎯 Research Interests

- **Computational Reactor Physics:** Deterministic neutron transport and diffusion, eigenvalue algorithms (power iteration, Krylov methods), heterogeneous multi-region core modeling.
- **Time-Dependent Reactor Dynamics:** Stiff kinetic equations, delayed-neutron multi-family kinetics, reactor control dynamics, reactivity accident analysis.
- **Stiff Numerical Time-Integration:** A-stable and L-stable multi-step and implicit Runge-Kutta schemes (BDF2, TR-BDF2, Radau IIA), high-frequency oscillation damping, order verification.
- **Scientific Machine Learning (SciML):** Physics-informed neural networks (PINNs), neural ODEs for physical dynamical systems, operator learning for parametric PDE acceleration.

---

## 🛠️ Technical Competencies

```
┌────────────────────────────────────────────────────────────────────────────────────────┐
│                                   RESEARCH TOOLKIT                                     │
├───────────────────────┬──────────────────────────┬─────────────────────────────────────┤
│ REACTOR PHYSICS       │ NUMERICAL ANALYSIS       │ SCIENTIFIC COMPUTING & ML           │
├───────────────────────┼──────────────────────────┼─────────────────────────────────────┤
│ • 1D Neutron Diffusion│ • Stiff ODE Solvers      │ • Python (NumPy, SciPy, Matplotlib) │
│ • Point Kinetics PRKE │   (BDF2, CN, Euler)      │ • PyTorch & Autograd / SciML        │
│ • 6-Group Delayed Pre.│ • Radau IIA Reference    │ • Git & GitHub Collaborative Dev    │
│ • Inhour Eigenvalues  │ • Finite Difference (FDM)│ • Automated Testing (Pytest)        │
│ • Criticality & Power │ • Thomas Algorithm (TDMA)│ • LaTeX / Academic Documentation    │
│ • Reflector Savings   │ • Convergence & Stability│ • Linux & Shell Scripting           │
└───────────────────────┴──────────────────────────┴─────────────────────────────────────┘
```

---

## 🎓 Education & Academic Background

- **B.Sc. in Nuclear Engineering**
  - **Core Coursework:** Nuclear Reactor Theory, Reactor Physics & Kinetics, Computational Methods in Nuclear Engineering, Engineering Mathematics, Partial Differential Equations (PDEs), Radiation Measurement & Shielding.
  - **Research Focus:** Applying rigorous numerical analysis and scientific computing to time-dependent and spatial reactor physics problems.

---

## 📬 Contact & Academic Inquiries

I am actively seeking **M.Sc. / Ph.D. graduate positions and funded Research Assistantships (RA)** in **Computational Nuclear Engineering, Reactor Physics, and Scientific Computing**.

- **Email:** [arashrezaii28@gmail.com](mailto:arashrezaii28@gmail.com)
- **GitHub:** [github.com/Arashsyberbrother](https://github.com/Arashsyberbrother)
- **LinkedIn:** [Arash Mohammadrezaei](https://linkedin.com)
- **Location:** Tehran, Iran (Open to Global Relocation)

<br/>

<div align="center">
  <sub><i>"Rigorous mathematical verification, transparent numerical analysis, and fundamental physics principles form the bedrock of predictive computational nuclear engineering."</i></sub>
</div>
