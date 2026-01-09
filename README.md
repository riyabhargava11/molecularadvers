This repo contains a Python script for analyzing the sensitivity of molecular energy predictions on the QM9 dataset under adversarial perturbations. The script was originally developed in Google Colab and is designed to run on CPU or GPU.

---

workflow:
1. Loads QM9 molecular data and model predictions
2. Applies adversarial perturbations (e.g. FGSM, PGD-style attacks)
3. Computes:
   - Absolute energy differences
   - Energy differences normalized per atom
4. Aggregates statistics across molecules
5. Generates summary plots and CSV outputs

---

## Files

- `quantum_chem_bhargava,_riya.py`  
  Main analysis script. 

---

## Outputs

Running the script generates the following files:

- `qm9_attacks_per_molecule.csv`  
  Per-molecule adversarial energy deviations

- `qm9_attacks_summary_raw.csv`  
  Summary statistics of absolute energy changes

- `qm9_attacks_summary_per_atom.csv`  
  Summary statistics normalized by number of atoms

Additionally, diagnostic plots are generated while execution, including:
- |ΔE| vs number of atoms
- Per-attack sensitivity comparisons

---

## Requirements

The script requires:

- Python ≥ 3.8
- PyTorch
- NumPy
- pandas
- matplotlib
- seaborn

