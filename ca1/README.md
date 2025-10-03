# Exercise 1 — Linear Transformations, Coordinate Systems, and Rank Geometry
Notebooks:
- ex1-linear-transformations-and-coordinate-systems.ipynb (instructor/piloted)
- ex1-linear-transformations-and-coordinate-systems_raw.ipynb (student/raw)
---
## Overview

This exercise develops core geometric intuitions behind linear algebra by treating matrices as transformations of space and vectors as coordinate-dependent objects. Students visualize how different linear maps deform a grid, how a vector’s coordinates change under a new basis, and how the rank of a matrix constrains the geometry of its image (collapse to a point/line/plane, or a full-dimensional embedding). The notebook combines step-by-step derivations with 2D and 3D visualizations (matplotlib and Plotly).

---

## Learning Objectives

By the end of this exercise, students should be able to:
1. Interpret matrices as linear maps from \( \mathbb{R}^n \to \mathbb{R}^m \) and connect algebraic operations to geometric effects.
2. Express vectors in different coordinate systems and compute basis changes using \( T^{-1} \).
3. Relate rank to geometric image: recognize when a transformation collapses a grid to a point (rank 0), a line (rank 1), a plane (rank 2), or preserves full 3D volume (rank 3).
4. Distinguish domain vs. codomain effects across \( 2\times 2 \), \( 3\times 2 \), and \( 3\times 3 \) mappings.
5. Visualize and reason about image, loss of dimensions, and the role of column spaces using plots.

---

## Key Concepts and Intuitions Covered

- **Vectors and Coordinates**
  - Vectors as coordinate tuples relative to a basis; the same geometric vector admits different coordinate representations.
  - Change of coordinates via a basis matrix \( T \) whose columns are the new basis vectors: \( x_{\text{new}} = T^{-1} x_{\text{std}} \).
  - Visual decomposition of a vector into basis components.

- **Matrices as Transformation Tools**
  - Matrices as linear transformations acting on grids of points; deformations such as rotations, shears, stretches, and projections.
  - Side-by-side plots of the original domain grid and its transformed image for immediate geometric interpretation.

- **Rank and Geometry of the Image**
  - Rank 0 (zero map): entire domain collapses to a single point.
  - Rank 1: domain collapses to a line (image lies in a 1D subspace).
  - Rank 2 (for \( 3\times 2 \) and \( 3\times 3 \)): image lies in a plane in \( \mathbb{R}^3 \).
  - Rank 3 (for \( 3\times 3 \)): full-rank mapping of \( \mathbb{R}^3 \) (invertible; preserves dimension).
  - Intuition: column space determines the image; dependent columns reduce dimensionality.

- **Coordinate vs. Geometry**
  - Differentiating the geometric vector from its coordinate representation in different bases.
  - Understanding how basis choice simplifies reasoning about a transformation.

- (Optional extensions present in the piloted notebook)
  - A simple transformation pipeline illustrating multiple cases (\( \mathbb{R}^2\to\mathbb{R}^2 \), \( \mathbb{R}^2\to\mathbb{R}^3 \), \( \mathbb{R}^3\to\mathbb{R}^3 \)).
---
## Backbone topics explicitly emphasized and thoroughly visualized:
**linear transformations**, vectors in **different coordinates**, **transformation matrices**, and the **effect of rank on transformations**.

---

## Notebook Roadmap

The two variants share the same conceptual structure; the piloted version adds complete implementations and polished visuals.

### Part A — Linear Transformations of Vectors
- Generate a 2D grid of points and apply various \( 2\times 2 \) matrices.
- Observe rotation, shear, and stretch effects.
- Discuss column vectors as images of basis vectors and their geometric meaning.

### Part B — Coordinate Representations
- Define a basis matrix \( T \) and compute \( x_{\text{new}} = T^{-1} x_{\text{std}} \).
- Plot the skewed grid defined by \( T \), show the basis vectors, and decompose a test vector in both bases.
- Emphasize why coordinates change while the underlying vector remains the same geometric arrow.

### Part C — Rank Inspection in Transformation Matrices
- Construct explicit matrices of different ranks and apply them to grids:
  - \( 3\times 2 \) case: \( \mathbb{R}^2 \to \mathbb{R}^3 \) (rank 0,1,2 images: point, line, plane).
  - \( 3\times 3 \) case: \( \mathbb{R}^3 \to \mathbb{R}^3 \) (rank 1,2,3 images: line, plane, full volume).
- Visualize with 3D scatter plots to see dimensional collapse or preservation.

### Piloted Notebook Enhancements
- Helper functions for grid generation and transformation pipelines.
- Plotly versions of the same scenes to facilitate interaction and inspection.
- Cleaner factorization of rank-specific matrix constructors.

---

## Prerequisites
- Familiarity with vectors, matrices, matrix–vector multiplication.
- Basic understanding of rank and column space.

---

## How to Use
- Raw version (students): complete the scaffolded code cells following the prompts in Parts A–C. Use plots to validate your intuition and answers.
- Piloted version (reference/solution): review complete implementations, compare outputs with your own, and use interactive views to deepen geometric understanding.
