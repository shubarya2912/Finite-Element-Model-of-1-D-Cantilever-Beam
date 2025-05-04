# Finite-Element-Model-of-1-D-Cantilever-Beam


This Python script performs **Finite Element Method (FEM)** analysis of a 1D cantilever beam under axial and bending loads using higher-order shape functions. It uses **quartic Lagrangian shape functions** for axial deformation and **cubic Hermitian shape functions** for bending deformation, ensuring improved accuracy for complex beam behavior.

## 📂 File Overview

**Filename:** `1D Cantilever Beam_FEM.py`

- Developed in Google Colab
- Focused on structural beam analysis using 4-node elements for axial and 2-node Hermite elements for bending

---

## 🚀 Features

- 4th-order Gauss quadrature integration
- Quartic axial shape functions (Lagrange interpolation)
- Cubic Hermite bending shape functions
- Mesh generation with 4 nodes per axial element
- Stiffness matrix and load vector calculation
- User-configurable beam properties via input prompts
- Plotting and visualization of results (if completed in full script)

---

## 🛠️ How to Run

```bash
python 1D\ Cantilever\ Beam_FEM.py
```

The script will prompt the user to enter beam parameters. Defaults are provided if the user presses Enter.

### Example Inputs

```text
Young's modulus (Pa) [default: 2e11]: 
Beam width (m) [default: 0.125]: 
Beam height (m) [default: 0.25]: 
Beam length (m) [default: 10]: 
Number of elements [default: 2]: 
Distributed load (N/m, downward negative) [default: -10000]: 
Axial point load at end (N, positive for tension) [default: 20000]:
```

---

## 🧮 Methodology

### Gauss Quadrature
Uses 4-point Gauss quadrature for integration to ensure accuracy for the higher-order shape functions.

### Shape Functions
- **Axial Deformation:** 4th-order Lagrangian functions with 4 nodes per element
- **Bending Deformation:** Cubic Hermitian functions with 2 nodes (each with displacement and rotation DOFs)

---

## 📦 Dependencies

- Python 3.x
- NumPy
- Matplotlib (for plots if included)

Install dependencies via:

```bash
pip install numpy matplotlib
```

---

## 📈 Output

- Nodal displacements (axial and bending)
- Reaction forces (if included in the final part)
- Optionally: displacement plots along the beam length

---

## 📚 Author

- **Name:** Shubham Kumar

---

## 📌 Notes

- The code structure is modular and allows easy extension to multiple elements and boundary conditions.
- Ensure you complete and verify functions like `compute_element_matrices` and the global assembly logic if not already included.
