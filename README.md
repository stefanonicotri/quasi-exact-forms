# Quasi-Exact Differential Forms & Hodge Decomposition

A standalone, interactive educational web tool exploring the concept of "quasi-exactness" in differential geometry. This project demonstrates how non-exact differential forms can be quantitatively measured for exactness using the **Hodge Decomposition Theorem**.

## 📌 Overview

In differential geometry and physics, path dependence is governed by a form's exterior derivative and the topology of the space. This project answers a specific question: *If a differential form is not perfectly exact, can we measure exactly how "quasi-exact" it is?*

By utilizing the Hodge Decomposition, this tool breaks down a path-dependent 1-form into perfectly orthogonal conservative (Exact) and swirling (Co-exact) components, allowing us to calculate a strict "percentage of exactness" based on the $L^2$ norms (energies) of the field.

## ✨ Features

* **Rigorous Mathematical Proofs:** Step-by-step derivations of the decoupled Poisson equations, Neumann/Dirichlet boundary conditions via Green's Theorem, and $L^2$ inner product normalizations. rendered beautifully via MathJax.
* **3D Surface Visualization:** Interactive, draggable 3D surface plots of the Exact and Co-exact scalar potentials calculated over a 2D unit disk, powered by Plotly.js.
* **Live Linear Field Analyzer:** A real-time interactive tool that instantly calculates the symmetric and anti-symmetric Hodge components of any linear differential form $\omega = (Ax + By)dx + (Cx + Ey)dy$, complete with a dynamic progress bar showing the field's quasi-exactness percentage.

## 🧮 Mathematical Background

On a closed Riemannian manifold, any differential $k$-form $\omega$ can be uniquely decomposed into three orthogonal components:
$$\omega = d\alpha + \delta\beta + \gamma$$

1.  **$d\alpha$ (Exact Component):** Path-independent gradient flow.
2.  **$\delta\beta$ (Co-Exact Component):** Divergence-free, rotational flow.
3.  **$\gamma$ (Harmonic Component):** Global topological flows (zero in $\mathbb{R}^2$).

By enforcing strict boundary conditions (Neumann for the exact part, Dirichlet for the co-exact part) on a finite domain like a unit disk, we guarantee perfect $L^2$ orthogonality. This allows us to define the quasi-exactness of the field as the ratio:
$$\text{Percentage Exact} = \frac{\|d\alpha\|^2}{\|\omega\|^2}$$

## 🛠️ Technologies Used

This project was intentionally built without heavy frontend frameworks (like React or Vue) or build tools (like Webpack or Vite) to ensure it remains a perfectly portable, zero-dependency educational resource.

* **HTML5 & Vanilla CSS3:** Used for the responsive layout, typography, and interactive sliders. All styling is self-contained within the file to guarantee it renders perfectly on GitHub Pages or any local machine.
* **Vanilla JavaScript (ES6):** Powers the "Interactive Linear Field Analyzer." It dynamically calculates the symmetric and anti-symmetric Hodge components, computes the $L^2$ norms, and updates the DOM in real time without needing a Python backend.
* **[MathJax (v3)](https://www.mathjax.org/):** A JavaScript display engine used to render the formal LaTeX equations—such as the Laplace-de Rham operator, codifferentials, and integrals—beautifully across all browsers.
* **[Plotly.js](https://plotly.com/javascript/):** A high-level, declarative charting library built on top of WebGL. It is used to generate the interactive, draggable 3D surface plots of the exact and co-exact scalar potentials.

## 👨‍💻 Author

**Stefano Nicotri**

* **GitHub:** [@stefanonicotri](https://github.com/stefanonicotri)

*(Feel free to reach out with questions, discussions on differential geometry, or contributions to this educational tool!)*

## License
This work is licensed under a Creative Commons Attribution-NonCommercial 4.0 International License.
