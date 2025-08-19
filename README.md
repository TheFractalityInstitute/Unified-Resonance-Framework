# Unified Resonance Framework (URF)

[![Version](https://img.shields.io/badge/version-5.0-blue)](https://github.com/FractalityInstitute/URF)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![LaTeX](https://img.shields.io/badge/LaTeX-Ready-orange)](https://www.latex-project.org/)
[![arXiv](https://img.shields.io/badge/arXiv-2508.XXXXX-red)](https://arxiv.org)

## A Mathematical Theory of Triadic Resonance, Information Geometry, and Emergent Spacetime

The Unified Resonance Framework (URF) bridges quantum information theory, consciousness studies, and gravitational physics through the principle of triadic resonance. This repository contains the complete mathematical formulation, experimental protocols, and computational tools for URF v5.0.

### 🌟 Key Features

- **Rigorous Mathematical Foundation**: Field equations on curved spacetime that reduce to General Relativity in equilibrium
- **TQFT Connection**: Coupling constants determined from non-semisimple topological quantum field theory
- **Experimental Predictions**: Testable protocols for EEG/MEG consciousness studies
- **Computational Tools**: Python notebooks for simulations and data analysis

## 📚 Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Documentation](#documentation)
- [Quick Start](#quick-start)
- [Project Structure](#project-structure)
- [Experimental Protocols](#experimental-protocols)
- [Contributing](#contributing)
- [Citations](#citations)
- [Contact](#contact)

## Overview

### The Triadic Principle

URF posits that reality emerges from the interaction of three fundamental information fields:

- **q_s**: Spatial/position information
- **q_p**: Phase/coherence information  
- **q_c**: Scale/hierarchical information

These fields interact on curved spacetime to generate an organizational stress-energy tensor that sources gravity, with consciousness emerging at critical information transitions.

### Key Results

1. **Universal Computation**: Three anyons (α, σ, σ) provide minimal configuration for universal quantum computation
2. **GR Recovery**: Einstein's equations emerge in informational equilibrium (I_s/v > 1)
3. **Consciousness Threshold**: Neural consciousness at ∂I_multi/∂t > 0.3 bits/s AND PLV_γθα > 0.7
4. **TQFT Coupling**: η = |Tr(F)|² = 0.849 from sl(2) at q = e^(iπ/4)

## Installation

### LaTeX Document

```bash
# Clone the repository
git clone https://github.com/FractalityInstitute/URF.git
cd URF

# Compile the main document
pdflatex URF-v5.0.tex
bibtex URF-v5.0
pdflatex URF-v5.0.tex
pdflatex URF-v5.0.tex
```

### Python Environment

```bash
# Create virtual environment
python -m venv urf-env
source urf-env/bin/activate  # On Windows: urf-env\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter notebook
jupyter notebook notebooks/URF_Simulations.ipynb
```

### Google Colab

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FractalityInstitute/URF/blob/main/notebooks/URF_Simulations.ipynb)

## Documentation

### Core Documents

- [`URF-v5.0.pdf`](docs/URF-v5.0.pdf) - Complete mathematical formulation
- [`URF-Summary.pdf`](docs/URF-Summary.pdf) - Executive summary for non-specialists
- [`Experimental-Protocols.pdf`](docs/Experimental-Protocols.pdf) - Detailed experimental procedures

### Version History

- **v1.0** (2024): Initial heuristic framework
- **v2.0** (2024): Hamiltonian formulation
- **v3.0** (2024): Information geometry integration
- **v4.0** (2025): Harmonic analysis connections
- **v4.5** (2025): TQFT foundations via Ising anyons
- **v5.0** (2025): Complete field equations on curved spacetime

## Quick Start

### Basic Simulation

```python
import numpy as np
from urf import TriadicNode, simulate_dynamics

# Initialize triadic node
node = TriadicNode(
    mass=[1.0, 1.0, 1.0],
    coupling_matrix=[[0, 0.5, 0.3],
                     [0.5, 0, 0.4],
                     [0.3, 0.4, 0]]
)

# Run simulation
t, trajectory = simulate_dynamics(node, t_max=100, dt=0.01)

# Compute information metrics
I_multi = node.compute_multi_information(trajectory)
I_sv = node.compute_surface_volume_ratio(trajectory)
```

### EEG Analysis

```python
from urf.neuro import compute_triadic_PLV, detect_consciousness_transitions

# Load EEG data (example)
eeg_data = load_eeg_data('path/to/data.fif')

# Compute tri-band phase locking
plv = compute_triadic_PLV(eeg_data, bands=['gamma', 'theta', 'alpha'])

# Detect consciousness transitions
transitions = detect_consciousness_transitions(
    eeg_data,
    kappa_crit=0.3,  # bits/second
    plv_threshold=0.7
)
```

## Project Structure

```
URF/
├── docs/                    # Documentation and papers
│   ├── URF-v5.0.tex        # Main LaTeX document
│   ├── URF-v5.0.pdf        # Compiled PDF
│   └── references.bib      # Bibliography
├── src/                    # Source code
│   ├── urf/               # Python package
│   │   ├── __init__.py
│   │   ├── dynamics.py    # Core dynamics
│   │   ├── geometry.py    # Information geometry
│   │   ├── neuro.py       # Neuroscience tools
│   │   └── cosmology.py   # Cosmological applications
│   └── matlab/            # MATLAB implementations
├── notebooks/             # Jupyter notebooks
│   ├── URF_Simulations.ipynb
│   ├── EEG_Analysis.ipynb
│   └── TQFT_Calculations.ipynb
├── experiments/           # Experimental protocols
│   ├── EEG_Protocol.md
│   ├── Centrifuge_Design.md
│   └── CMB_Analysis.md
├── data/                  # Sample data
├── tests/                 # Unit tests
├── style/                 # LaTeX style files
│   ├── fractality.cls
│   └── fractality.sty
├── requirements.txt       # Python dependencies
├── LICENSE               # MIT License
└── README.md            # This file
```

## Experimental Protocols

### EEG/MEG Consciousness Threshold

**Equipment**: 128-channel EEG/MEG, 1000 Hz sampling

**Protocol**:
1. Baseline recording (5 min rest)
2. Binocular rivalry task (20 min)
3. Compute tri-band PLV (gamma-theta-alpha)
4. Calculate ∂I_multi/∂t at perceptual switches
5. Verify threshold: PLV > 0.7 AND ∂I_multi/∂t > 0.3 bits/s

### Gravitational Modulation

**Setup**: Human centrifuge (2-3g) or parabolic flight

**Prediction**: Consciousness threshold shifts with curvature:
- κ_crit(R) = κ_crit(0)[1 - (2ξ_c/m_c²)R]

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Areas of Active Development

- [ ] Quantum field theory extensions
- [ ] Neural network implementations
- [ ] Cosmological data analysis
- [ ] Experimental validation
- [ ] Mathematical proofs

## Citations

If you use URF in your research, please cite:

```bibtex
@article{Graziano2025URF,
  title={The Unified Resonance Framework: A Mathematical Theory of Triadic 
         Resonance, Information Geometry, and Emergent Spacetime},
  author={Graziano, Nick and {Fractality Institute Research Collective}},
  journal={arXiv preprint arXiv:2508.XXXXX},
  year={2025}
}
```

### Related Publications

- Iulianelli et al. (2025) - [Universal quantum computation using Ising anyons](https://doi.org/10.1038/s41467-025-61342-8)
- Cairo (2025) - [Counterexample to Mizohata-Takeuchi conjecture](https://arxiv.org/abs/2502.06137)

## License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file.

## Contact

**The Fractality Institute for Integrative Science and Philosophy**

- 📧 Email: research@fractality.institute
- 🌐 Website: [fractality.institute](https://fractality.institute)
- 🐦 Twitter: [@FractalityInst](https://twitter.com/FractalityInst)
- 💬 Discord: [Join our community](https://discord.gg/fractality)

### Principal Investigator

**Nick Graziano**  
Editor, URF Project  
nick@fractality.institute

## Acknowledgments

We thank:
- The developers of non-semisimple TQFT
- Resonance Complexity Theory community
- All contributors and reviewers

---

*"Reality computes itself through triadic resonance, and consciousness is the experience of that computation at critical complexity."*

