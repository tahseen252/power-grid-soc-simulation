# Network Dynamics and Self-Organized Criticality in Power Grid Failure Cascades

**Complexity Science Course Project**

## Overview

This project applies complexity science concepts — specifically **Self-Organized Criticality (SOC)** — to model cascading failure dynamics in electrical power grids. A power transmission network is simulated as a graph where random load perturbations can trigger cascading blackouts (avalanches) that propagate through the network.

## Key Findings

- Avalanche-size distribution follows a **power law** with exponent α ≈ 2.31
- **Scale-free networks** (resembling real power grids) produce the heaviest-tailed cascade distributions
- Large avalanches correlate strongly with **connectivity drops** in the network
- The system **self-organizes to criticality** without parameter tuning

## Repository Structure

```
├── power_grid_soc.py      # Main simulation code (Python)
├── report.tex             # LaTeX manuscript source
├── report.pdf             # Compiled PDF report
├── figures/               # Generated figures
│   ├── network.png
│   ├── degree_distribution.png
│   ├── avalanche_timeseries.png
│   ├── freq_distribution.png
│   ├── connectivity.png
│   ├── conn_vs_avalanche.png
│   ├── topology_comparison.png
│   └── stats.json
└── README.md
```

## Requirements

```
Python >= 3.8
numpy
networkx
matplotlib
scipy
```

## Running the Simulation

```bash
python power_grid_soc.py
```

This will run the full simulation (~20,000 time steps) and generate all figures in the `figures/` directory.

## Model Description

| Component | Implementation |
|-----------|----------------|
| **Noise** | Random load injection at random alive nodes each time step |
| **Avalanche** | Overloaded nodes fail and redistribute load to alive neighbours |
| **Connectivity** | Measured via largest connected component fraction |
| **Repair** | Slow stochastic repair when >30% of nodes have failed |

Three network topologies are compared: Scale-Free (Barabási–Albert), Small-World (Watts–Strogatz), and Random (Erdős–Rényi).

## Acknowledgements

- Developed with assistance from Claude (Anthropic)
- Built using NetworkX, NumPy, SciPy, and Matplotlib
