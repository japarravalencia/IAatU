# Mitigating Cognitive Offloading & Surrender in AI-Augmented Software Engineering Cohorts (4.5-Year System Dynamics Simulator)

[![Live Simulator](https://img.shields.io/badge/Live_RK4_Simulator-GitHub_Pages-008080?style=for-the-badge)](https://japarravalencia.github.io/ai-cognitive-sovereignty-sd/)
[![Zenodo DOI](https://img.shields.io/badge/Zenodo_DOI-10.5281%2Fzenodo.XXXXXXX-0f2648?style=for-the-badge)](https://doi.org/10.5281/zenodo.XXXXXXX)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg?style=for-the-badge)](https://creativecommons.org/licenses/by/4.0/)

Interactive Open Science replication package accompanying the manuscript submitted to *IEEE Transactions on Education*:

> **Parra Valencia, J. A., & Taylor, I. (2026).** *Mitigating Cognitive Offloading and Surrender in AI-Augmented Software Engineering Cohorts: A Multiscale System Dynamics Assessment of "Brain-First" and "Dual-Clock" Curricular Architectures.* IEEE Transactions on Education (submitted).

## Launch Interactive Simulator (No Installation Required)
- **Web Flight Simulator (GitHub Pages):** https://japarravalencia.github.io/ai-cognitive-sovereignty-sd/
- **Permanent Archive (Zenodo):** https://doi.org/10.5281/zenodo.XXXXXXX *(update after Zenodo release)*

## Repository Contents
- `index.html` — Standalone browser-based fourth-order Runge-Kutta (RK4, $\Delta t = 0.125$ wk, 234 weeks) interactive simulator with all 7 published scenarios (`P1`–`P4`, `P3b Late Remediation`, `Extreme 1`, `Extreme 2`), live policy sliders, interactive feedback loop explorer (`R1`, `B2`, `B4`, `B5`, `B6`), embedded model equations, and one-click CSV export.
- `AI y Soberania Cognitiva IdeS sfd.stmx` — Native OASIS XMILE 1.0 model file (Stella Architect) with 9 stocks, 13 flows, 12 auxiliaries, 36 constants, and 35 auditable `LOOPSCORE` LTM variables.
- `experimentos_soberania_rk4_sobol.py` — Deterministic Python RK4 replication script running all 7 scenarios, RK4 step-size convergence ($\Delta t = 0.125$ vs. $0.0625$ wk), Barlas zero-flow/extreme tests, and global Sobol sensitivity (`SALib`).
- `corridas_csv/` — Precomputed verified scenario trajectories (`01_P1_Baseline.csv` through `06_Extreme2_MaxCollapse.csv`).

## Local Python Replication
```bash
pip install numpy pandas SALib
python experimentos_soberania_rk4_sobol.py --proyecto 2026_nuevo_paper_piloto


License & Citation

Released under CC-BY 4.0 (documentation/data) and MIT (verification scripts). Please cite the accompanying manuscript and Zenodo DOI when reusing the model or simulator.
