# Multi-View Consistent 3D Generation: MVDream

An academic survey and comparative analysis exploring multi-view diffusion models for consistent 3D asset synthesis, addressing classical 2D-lifting pitfalls like the multi-face Janus problem and content drift.

---

### Overview

Generating 3D representations from generative 2D priors (2D-lifting via Score Distillation Sampling) often suffers from critical spatial inconsistencies:
* **The Multi-Face Janus Problem:** Models regenerate redundant features (e.g., multiple faces or fronts) across varying viewpoints due to a lack of 3D multi-view awareness.
* **Content Drift:** Subject identity, textures, and geometry distort as the camera angle changes.

This paper synthesizes the architectural mechanisms of **MVDream**—which learns a joint multi-view diffusion distribution parameterized by camera poses and cross-view attention—and compares it with **ImageDream**, contrasting text-driven versus image-conditioned 3D generation.

---

### Key Insights

* **Architecture & Multi-View Consistency:** Analysis of MVDream’s UNet integrating 3D self-attention across camera viewpoints, enforcing spatial integrity during a single diffusion pass.
* **Comparative Evaluation (MVDream vs. ImageDream):**
  * *MVDream:* High creative flexibility from text prompts, but higher memory footprint and resolution trade-offs.
  * *ImageDream:* Leverages image-prompt conditioning and multi-level controllers to anchor fine surface details, textures, and geometry.
* **Real-World Applications:** Use cases in automated 3D asset pipelines for indie game development (via Multi-View DreamBooth) and digital twins for e-commerce.

---

### Report Access

The complete essay including architectural diagrams, visual comparisons, and mathematical formulations is available directly in this repository:

📄 **[Download the Full Report (PDF)](https://github.com/martina-cisotto/MVDream.pdf)**

---

### References & Literature

This report analyzes and builds upon foundational works in 3D generative diffusion:
* **MVDream:** Shi, Y., Wang, P., Ye, J., Mai, L., Li, K., & Yang, X. (2024). *MVDream: Multi-view diffusion for 3D generation*.
* **ImageDream:** Wang, P., & Shi, Y. (2023). *ImageDream: Image-prompt multi-view diffusion for 3D generation*. 
* **DreamFusion:** Poole, B., Jain, A., Barron, J. T., & Mildenhall, B. (2023). *DreamFusion: Text-to-3D using 2D diffusion*. ICLR.
* **DreamBooth:** Ruiz, N., Li, Y., Jampani, V., Pritch, Y., Rubinstein, M., & Aberman, K. (2023). *DreamBooth: Fine tuning text-to-image diffusion models for subject-driven generation*. CVPR.
