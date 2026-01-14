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

Block-encoding (FABLE):
- **fable-circuits** (PyPI): https://pypi.org/project/fable-circuits/1.0.2/



### Install
```bash
- pip install fable-circuits==1.0.2


## Citation A formal citation will be added once the associated paper/proceedings version is published. In the meantime, please reference this repository URL when using the code: - https://github.com/raminsalehi1993/dqc1-entropy-clustering

### FABLE (block-encoding circuits)
If you use the FABLE block-encoding component, please cite:

Daan Camps and Roel Van Beeumen, **“FABLE: Fast Approximate Quantum Circuits for Block-Encodings,”**
*2022 IEEE International Conference on Quantum Computing and Engineering (QCE)*, 2022.  
arXiv:2205.00081.
