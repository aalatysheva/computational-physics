# Computational Physics

A collection of computational physics projects implementing numerical methods from scratch, analysing their accuracy and convergence, and applying them to physical problems.


## Projects

### [Quantum Well](quantum-well/)

Numerical solution of a **triangular finite quantum well** (Schrödinger equation, bound-state eigenvalue problem), benchmarked against the analytical Airy-function solution.

- Finite-difference eigenvalue solver and shooting-method / matching-determinant approach for bound states
- Convergence of numerical eigenvalues to the analytical ones as grid resolution increases (`∝ N⁻²`)
- Sensitivity of bound-state energies to the size of the computational box
- Visualization of wavefunctions, probability densities, and energy levels

**Notebook:** [`triangular_well.ipynb`](quantum-well/triangular_well.ipynb)

### [Numerical Methods](numerical-methods/)

Three labs covering the core toolbox of numerical analysis, each with convergence/accuracy studies rather than just implementations.

| Lab | Notebook | Topics |
|---|---|---|
| 1 — Linear Algebra & Nonlinear Equations | [`SLAE_solutions.ipynb`](numerical-methods/SLAE_solutions.ipynb) | Gaussian elimination, LU, Cholesky, Jacobi, Gauss–Seidel, Newton, secant, multidimensional Newton |
| 2 — Interpolation, Differentiation, Integration | [`interpolation_differentiation_integration_methods.ipynb`](numerical-methods/interpolation_differentiation_integration_methods.ipynb) | Lagrange & spline interpolation, finite differences, Simpson's rule, Monte Carlo integration |
| 3 — ODEs | [`differential_equations.ipynb`](numerical-methods/differential equations.ipynb) | Euler, RK4, Adams, stiff systems, boundary-value problems via shooting method |

See [`numerical-methods/README.md`](numerical-methods/README.md) for the full breakdown of methods and experiments in each lab.

## Methods and Tools

- **Language:** Python (NumPy, SciPy, Matplotlib)
- **Numerical methods:** linear algebra solvers, root-finding, interpolation, numerical differentiation/integration, ODE integrators, boundary-value and eigenvalue problems
- **Analysis:** convergence order, numerical stability, error estimation, sensitivity to initial/boundary conditions

## Running the notebooks

```bash
pip install -r requirements.txt
jupyter notebook
```

## About

These projects focus on implementing numerical methods from scratch, analysing their accuracy and convergence, and applying them to physical problems in quantum mechanics and applied mathematics.
