---
title: "Probability-Aware Multiple Instance Learning for Patch-to-Slide Prediction in Multi-Gigapixel Whole-Slide Images"
order: 3
image: /images/projects/Project3.png
---

#### Data

Addressed the critical challenge of label scarcity in female malignancies by conducting a large-scale study on 5,944 Whole-Slide Images and releasing a quasi-segmentation resource with model-assisted pseudo-labels to facilitate weakly supervised tumor localization without expensive pixel-level annotations.

#### Backbone

Implemented a hybrid CoAtNet-LS-SD encoder that synergizes MB-Conv and Transformers, enhancing the backbone with LayerScale and scheduled stochastic depth to calibrate residual branches. Yielded embedded features and instance-level tumor probabilities that directly initialize Top-k candidate mining for efficient aggregation.

#### Framework

Developed a probability-aware Gated-Attention MIL framework that fuses spatial and probability embeddings to suppress noise, achieving SOTA performance in slide-level classification and generating high-fidelity attention heatmaps for tumor localization.
