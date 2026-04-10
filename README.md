# Network Dynamics and Self-Organized Criticality in Power Grid Failure Cascades

**Complexity Science Course Project**

## Overview

This project applies complexity science concepts — specifically **Self-Organized Criticality (SOC)** — to model cascading failure dynamics in electrical power grids. A power transmission network is simulated as a graph where random load perturbations can trigger cascading blackouts (avalanches) that propagate through the network.

## Key Findings

- Avalanche-size distribution follows a **power law** with exponent α ≈ 2.31
- **Scale-free networks** (resembling real power grids) produce the heaviest-tailed cascade distributions
- Large avalanches correlate strongly with **connectivity drops** in the network
- The system **self-organizes to criticality** without parameter tuning



## Requirements

```
Python >= 3.8
numpy
networkx
matplotlib
scipy
```

