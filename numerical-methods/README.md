# Numerical Methods

A collection of numerical methods implemented in Python as part of computational physics and numerical mathematics laboratory projects.

The notebooks cover numerical linear algebra, nonlinear equations, interpolation, numerical differentiation and integration, ordinary differential equations, boundary-value problems, and stiff systems.

## Contents

### Lab 1 — Numerical Linear Algebra and Nonlinear Equations

**Notebook:** `SLAE_solutions.ipynb`

This laboratory focuses on direct and iterative methods for solving systems of linear algebraic equations (SLAE), as well as methods for solving nonlinear equations and systems.

#### Direct methods for linear systems

Implemented methods:

- Gaussian elimination with partial pivoting
- LU decomposition
- Cholesky decomposition for symmetric positive-definite matrices

The methods are tested on random nonsingular matrices and different types of structured matrices.

The experiments include:

- studying numerical stability and sensitivity to matrix conditioning;
- testing the methods on Hilbert matrices;
- comparing numerical errors and residuals;
- analysing diagonally dominant matrices;
- studying symmetric positive-definite matrices;
- investigating computational scalability for increasing system size.

The relative solution error

`||x - x*||₂ / ||x*||₂`

and the residual

`||Ax - b||₂`

are evaluated and compared with the condition number of the matrix.

#### Iterative methods for linear systems

Implemented methods:

- Jacobi method
- Gauss–Seidel method

The experiments investigate:

- convergence speed depending on the system size;
- the influence of diagonal dominance;
- the effect of changing diagonal elements;
- convergence behaviour for symmetric positive-definite matrices;
- the influence of the initial approximation.

The convergence criterion is based on the residual norm.

#### Nonlinear equations

Implemented methods:

- Newton's method
- Secant method
- Fixed-derivative (modified Newton) method

The methods are tested on several nonlinear functions. Their convergence behaviour is analysed by studying the residual at each iteration and determining the observed type of convergence.

The sensitivity of the methods to the initial approximation is also investigated.

#### Nonlinear systems

A multidimensional Newton method is implemented for systems of nonlinear equations.

The Jacobian is used to determine the Newton step, with the resulting linear system solved using direct methods such as LU decomposition or Gaussian elimination.

The experiments include:

- studying basins of convergence for different initial approximations;
- visualising iteration trajectories;
- comparing numerical results with analytical solutions.

---

### Lab 2 — Numerical Methods in Mathematical Analysis

**Notebook:** `interpolation_differentiation_integration_methods.ipynb`

This laboratory focuses on numerical approximation of functions, derivatives, and definite integrals.

#### Polynomial interpolation

Implemented:

- Lagrange interpolation for arbitrary interpolation nodes.

The experiments investigate the interpolation error depending on the number of nodes.

The Runge function

`f(x) = 1 / (1 + x²)`

is also considered on the interval `[-5, 5]` using a uniform grid. The behaviour of the interpolation is analysed, including the Runge phenomenon.

#### Spline interpolation

Spline interpolation is implemented for arbitrary interpolation grids.

The effect of different boundary conditions for the second derivatives is investigated and visualised using graphs.

#### Numerical differentiation

Finite-difference methods are implemented for calculating:

- the first derivative;
- the second derivative;
- the third derivative.

Differentiation using four equally spaced points is studied for different step sizes.

The numerical error is investigated for step sizes ranging from `10⁻¹` to `10⁻¹³` and for polynomials of different degrees.

A five-point formula for the second derivative is also derived and tested. The theoretical error estimate is compared with the actual numerical error for a smooth non-polynomial function.

#### Numerical integration

Implemented methods:

- rectangle method;
- trapezoidal rule;
- Simpson's rule;
- Simpson's 3/8 rule.

The methods are tested on functions including:

- `xⁿ`;
- `eˣ`;
- `sin(x)`.

The dependence of numerical accuracy on the step size is investigated and compared with theoretical expectations.

#### Monte Carlo integration

A probabilistic approach to numerical integration is implemented using Monte Carlo sampling.

The method is tested on a continuous function, and the dependence of the approximation accuracy on the number of random points is investigated.

---

### Lab 3 — Numerical Methods for Ordinary Differential Equations

**Notebook:** `differential equations.ipynb`

This laboratory focuses on numerical methods for ordinary differential equations, including initial-value problems, boundary-value problems, and stiff systems.

#### Initial-value problems

Implemented methods:

- Explicit Euler method
- Classical fourth-order Runge–Kutta method (RK4)
- Fourth-order Adams method

A second-order differential equation is reduced to a system of two first-order equations and solved numerically for different step sizes.

The numerical solution is compared with the analytical solution in order to estimate the error and determine the observed order of accuracy.

#### Stiff systems

The laboratory investigates the concept of stiffness and the difference between explicit and implicit numerical methods.

Implemented methods:

- Explicit Euler method
- Classical fourth-order Runge–Kutta method
- Implicit Euler method

The methods are applied to the stiff system

`y₁' = -1000y₁ + 999y₂`

`y₂' = -y₂`

with the specified initial conditions.

Numerical solutions are calculated for several step sizes and compared with the analytical solution.

The experiments investigate:

- numerical stability;
- the effect of increasing the integration step;
- the difference between explicit and implicit methods;
- the influence of stiffness on numerical integration.

#### Boundary-value problems

The shooting method is applied to the boundary-value problem

`y''(x) = -y(x)`

with boundary conditions

`y(0) = 0`

`y(π/2) = 1`.

The second-order equation is converted into a system of two first-order equations and solved using RK4.

The unknown initial derivative is determined using:

- the bisection method;
- Newton's method.

The convergence of the iterations is visualised and the numerical solution is compared with the analytical solution.

---

## Methods

| Area | Methods |
|---|---|
| Linear algebra | Gaussian elimination, LU decomposition, Cholesky decomposition |
| Iterative linear solvers | Jacobi, Gauss–Seidel |
| Nonlinear equations | Newton, Secant, Fixed-derivative |
| Nonlinear systems | Multidimensional Newton |
| Interpolation | Lagrange, spline interpolation |
| Numerical differentiation | Finite differences, five-point formula |
| Numerical integration | Rectangles, trapezoidal, Simpson, Simpson 3/8 |
| Probabilistic methods | Monte Carlo integration |
| ODEs | Euler, RK4, Adams |
| Stiff ODEs | Explicit Euler, RK4, implicit Euler |
| Boundary-value problems | Shooting method, bisection, Newton |

## Topics Investigated

The projects focus not only on implementing numerical algorithms, but also on analysing their practical behaviour:

- numerical accuracy;
- convergence;
- order of accuracy;
- numerical stability;
- matrix conditioning;
- sensitivity to initial conditions;
- error estimation;
- convergence rate;
- computational scalability;
- behaviour of explicit and implicit methods.

## Tools

- Python
- NumPy
- SciPy
- Matplotlib
- Jupyter Notebook
