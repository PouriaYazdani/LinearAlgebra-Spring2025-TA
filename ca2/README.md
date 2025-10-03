# Exercise 2 — Orthogonal Diagonalization, Quadratic Forms, and Constrained Optimization
Notebooks:
- ex2-orthogonal-diagonalization-quadratic-forms-optimization.ipynb (instructor/piloted)
- ex2-orthogonal-diagonalization-quadratic-forms-optimization_raw.ipynb (student/raw)
---
## Overview
This exercise deepens geometric understanding of symmetric matrices and their eigenstructure. In Part A, students practice orthogonal diagonalization of real symmetric matrices, interpret the transformation enacted by the diagonalization factors, and quantify reconstruction error when discarding eigen-directions (a foundation for SVD intuition). Part B develops intuition for quadratic forms through contour plots in both the eigenbasis and the standard Cartesian basis, clarifying how eigenvalues scale directions and how eigenvectors define principal axes. Part C connects quadratic forms to constrained optimization, analyzing the Rayleigh quotient and Lagrange-multiplier conditions; students characterize optimal values/vectors under one constraint, then observe how solutions evolve when additional constraints are imposed.

---

## Learning Objectives
1. Perform and interpret **orthogonal diagonalization** $A = Q \Lambda Q^\top$ for real symmetric $A$.
2. Explain the **geometric action** of $Q$ (basis alignment) and $\Lambda$ (axis-aligned scaling), and map vectors/contours between bases.
3. Compute and reason about **reconstruction error** when approximating $A$ (or data projected by $A$) using a subset of eigenpairs.
4. Analyze **quadratic forms** $x^\top A x$: identify principal axes, level sets, and definiteness from eigenvalues/eigenvectors.
5. Solve **constrained quadratic optimization** via the **Rayleigh quotient** and **Lagrange multipliers**; recognize the role of eigenvectors as optimal directions.
6. Extend the analysis to **multiple constraints**, relating to generalized eigenvalue problems and feasible subspaces.
---
## Key Concepts and Intuitions Covered
- **Spectral theorem (symmetric case)**: existence of an orthogonal eigenbasis; diagonalization $A = Q \Lambda Q^\top$.
- **Change of basis via $Q$**: coordinates $y = Q^\top x$ rotate/reflect data to align with eigenvectors; $\Lambda$ scales axes independently.
- **Reconstruction/approximation**: truncating small-magnitude eigenvalues/eigenvectors and measuring the induced error (e.g., energy captured, residual norm).
- **Quadratic forms**: $x^\top A x$ as weighted energy; level sets are ellipses/ellipsoids oriented by eigenvectors and scaled by eigenvalues.
- **Contours in two coordinate systems**:
  - **Eigenbasis**: contours are axis-aligned; values determined directly by $\Lambda$.
  - **Cartesian basis**: contours are rotated/scaled ellipses; $Q$ reorients axes.
- **Optimization with constraints**:
  - **Single constraint** (e.g., $\|x|=1$): extrema of $x^\top A x$ occur at eigenvectors; extremal values are eigenvalues (Rayleigh quotient).
  - **Multiple constraints**: feasible set becomes an affine/subspace intersection; solutions relate to **generalized eigenproblems** or projected optimization.
---
## Backbone topics explicitly emphasized and thoroughly:
**orthogonal diagonalization**, **eigenvalue–eigenvector geometry**, **quadratic forms and contours**, and **constrained optimization via the Rayleigh quotient/Lagrange multipliers**.

---

## Notebook Roadmap
The two variants share the same conceptual structure; the piloted version adds complete implementations and polished visuals.

### Part A — Orthogonal Diagonalization and Reconstruction Error
- Compute $Q,\Lambda$ for symmetric $A$ and verify $A = Q \Lambda Q^\top$.
- Visualize how $Q$ maps vectors to the eigenbasis and how $\Lambda$ scales each principal axis.
- Truncate eigenpairs (keep top-$k$) to build $A_k = Q \Lambda_k Q^\top$; compare outputs of $A$ vs. $A_k$.
- Quantify **reconstruction error** (e.g., $\|A - A_k\|$, or discrepancy on transformed vectors) and interpret energy captured by top eigenvalues.

### Part B — Quadratic Forms and Contour Analysis
- Plot level sets of $x^\top A x = c$ in **Cartesian coordinates** (rotated ellipses).
- Transform to **eigen-coordinates** $y = Q^\top x$ and re-plot the same contours; demonstrate axis alignment and per-axis scaling by $\Lambda$.
- Relate **definiteness** (sign pattern of eigenvalues) to the presence/shape of contours (ellipses, degenerate lines, saddle shapes).

### Part C — Constrained Optimization with Quadratic Forms
- Solve $\max/\min \; x^\top A x \; \text{subject to} \; \|x\|=1$ using the **Rayleigh quotient**; show solutions are eigenvectors with values $\lambda_{\max}$ and $\lambda_{\min}$.
- Implement **Lagrange multipliers** to derive $A x = \lambda x$ under the unit-norm constraint.
- Add a second constraint (e.g., linear constraint $B^\top x = d$ or orthogonality to a subspace) and observe how the solution changes:
  - Discuss **projected optimization** and connections to **generalized eigenvalue problems** when constraints are quadratic/linear.

### Piloted Notebook Enhancements
- Helper utilities for spectral decomposition, basis transforms, and error metric.
- Dual-contour plotting functions that render the **same quadratic form** in both eigen and Cartesian coordinates.
- Worked examples of single- and multi-constraint optimization with numerical verification of optimality conditions.
---
## Prerequisites
- Comfort with eigenvalues/eigenvectors, symmetric matrices, and positive (semi)definiteness.
- Prior exposure to change of basis and orthogonal matrices.
---
## How to Use
- **Student/raw version**: follow the scaffolded prompts to compute $Q,\Lambda$, construct truncated approximations, and generate contour/optimization plots. Fill in derivations and code where indicated.
- **Instructor/piloted version**: consult as a reference for complete implementations, expected outputs, and additional visual diagnostics.
