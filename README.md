# Linear Algebra — Teaching Materials

This repository contains three components for the Spring 2025 Linear Algebra course that I devised and piloted as a Teaching Assistant:
1) Exercise 1: Linear Transformations & Coordinate Systems
2) Exercise 2: Orthogonal Diagonalization, Quadratic Forms, and Constrained Optimization
3) Project: Latent-Factor–Based Recommender

Each component has its own detailed README and notebook(s). The exercises provide geometric intuition and foundational tools; the project applies these tools to build and evaluate a recommender system grounded in linear algebra.

---

## Components

### 1) Exercise 1 — Linear Transformations, Coordinate Systems, and Rank Geometry
- Notebooks:
  - ex1-linear-transformations-and-coordinate-systems.ipynb (instructor/piloted)
  - ex1-linear-transformations-and-coordinate-systems_raw.ipynb (student/raw)
- Focus:
  - Matrices as linear maps; geometric effects (rotation, shear, stretch, projection)
  - Vectors in different coordinate systems; change of basis via a basis matrix
  - Rank and the geometry of images (collapse to point/line/plane, dimension preservation)

### 2) Exercise 2 — Orthogonal Diagonalization, Quadratic Forms, and Constrained Optimization
- Notebooks:
  - ex2-orthogonal-diagonalization-quadratic-forms-optimization.ipynb (instructor/piloted)
  - ex2-orthogonal-diagonalization-quadratic-forms-optimization_raw.ipynb (student/raw)
- Focus:
  - Orthogonal diagonalization of symmetric matrices and reconstruction error (PCA intuition)
  - Quadratic forms and contour analysis in eigen vs. Cartesian coordinates
  - Constrained optimization (Rayleigh quotient, Lagrange multipliers; multiple constraints)

### 3) Project — Latent-Factor–Based Recommender
- Notebook:
  - project-latent-factor-based-recommender.ipynb (instructor/piloted)
- Focus:
  - User–item matrix modeling; cosine similarity (user–user / item–item)
  - Matrix factorization with regularization and bias terms; rating prediction & top-N ranking
  - Latent factor based analysis and basic clustering in latent space.

---

## Intended Audience and Usage
- **Students:** start with the **_raw** versions and follow prompts; compare to the piloted versions after completion.
- **Instructors/TAs:** use piloted versions for reference solutions, additional diagnostics, and visualizations.

