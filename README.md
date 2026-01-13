# DQC1 Entropy Clustering (Normalized-Trace Kernel)

This repository provides a hybrid quantum–classical clustering pipeline based on **Deterministic Quantum Computation with One Qubit (DQC1)** and **Rényi-2 entropy**. The implementation compares:

1. **DQC1 FULL**: DQC1 normalized-trace kernel + DQC1 purity-based ΔH assignments + entropy-guided reduction + automatic **K\*** selection  
2. **Parzen FULL**: Gaussian Parzen kernel + ΔH assignments + reduction + automatic **K\*** selection  
3. **K-Means baseline**: K fixed to the ground-truth number of classes

The DQC1 pipeline supports multiple quantum feature maps (`zz`, `zdiag`, `rxryrz`, `pauli`, `karimi`) and evaluates cluster entropies via **FABLE block-encoding** and DQC1 trace estimation.

## Implemented datasets (synthetic)
- `spirals`
- `rings_factor02` (rings with thickness factor = 0.2)
- `moons`
- `circles`
- `anistropic_blobs`

## Requirements
Core:
- Python 3.10+ (recommended)
- `numpy`, `scipy`, `pandas`, `matplotlib`
- `scikit-learn`
- `joblib`

Quantum + simulation:
- `qiskit`, `qiskit-aer`
- `torch` (CPU or CUDA for acceleration)
- `fable` (must expose `from fable import fable as fable_build`)

## Running
Run the main script directly:
```bash
python <YOUR_SCRIPT_NAME>.py


## Citation
A formal citation will be added once the associated paper/proceedings version is published.  
In the meantime, please reference this repository URL when using the code:
- https://github.com/raminsalehi1993/dqc1-entropy-clustering
