---
title: "Controllable Medical Synthetic Data with Constrained Diffusion Models"
order: 1
image: /images/projects/Project1.png
---

#### Formulation

Formulated multimodal MRI synthesis and completion by learning a joint distribution instead of separate task-specific conditional mappings. The formulation shares global brain morphology and anatomical structures for high-efficiency training or steering; a well-learned joint distribution induces all required conditional distributions mathematically, allowing scarce or incompletely observed modalities to benefit from shared data while preserving 3D continuity and subject-level cross-modal consistency.

#### Method

Converted a pretrained brain MRI generator designed for one modality at a time into a joint multimodal model by introducing a dynamic spatial Adapter that simultaneously reads observed modalities and evolving target states. The Adapter (essentially a 3D-UNet) learns their shared anatomy and contrast-specific relationships and mediates information exchange throughout generation, retaining the pretrained image prior while enabling multimodal co-generation and flexible completion.

#### Applications

Targeted two complementary applications: co-generating multimodal MRI studies to augment scarce datasets for downstream model training, and completing unacquired sequences from a patient's partial MRI examination. The unified framework accommodates different observation patterns without maintaining a separate generator for every missing-modality configuration, while keeping multiple synthesized targets mutually consistent.
