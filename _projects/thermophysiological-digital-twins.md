---
title: "Human Thermophysiological Digital Twins: Physics-Constrained Spatiotemporal Forecasting with Neural Mixture of Experts"
order: 2
image: /images/projects/Project2.png
---

#### Data

Addressed the scarcity of comprehensive physiological data by refactoring the JOS-3 simulator to generate 3M+ pre-training samples and integrating constraints derived from the Pennes bioheat equation to strictly enforce thermodynamic energy conservation laws, creating a robust hybrid data-and-physics-driven base model.

#### Architecture

Engineered a Physics Informed Transformer-MoE architecture where a Sparse Mixture-of-Experts mechanism with a gating router adaptively maps neural experts to specific anatomical segments, effectively capturing the intermediate physiological parameters (e.g., blood flow, sweat rate) between the stable core and dynamic extremities.

#### Outcome

Delivered subject-conditioned forecasts of core and regional skin temperatures together with heat-flux-derived regulatory states, making the model's physiological behavior examinable rather than treating it as a black box. The framework provides a basis for evaluating thermal exposure scenarios in advance and for future applications in occupational heat-risk management.
