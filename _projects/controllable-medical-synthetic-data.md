---
title: "Controllable Medical Synthetic Data with Constrained Diffusion Models"
order: 1
image: /images/projects/Project1.png
---

#### Formulation

Formulated multimodal image synthesis and completion as learning one joint distribution over modalities instead of separate task-specific conditional mappings, with multi-contrast brain MRI as the driving application. A well-learned joint distribution induces every conditional mathematically, so a single model covers both generation and completion for any pattern of missing modalities. Because training targets the marginal of whichever modalities are present in each sample, scarce or incompletely observed modalities still benefit from shared anatomy, and datasets with different modality sets can be pooled without imputation or complete pairs.

#### Method

Designed a branched joint-diffusion architecture with a clear division of labor. A shared denoising backbone learns the generation quality of each individual modality, while cross-modal adapter branches learn the alignment between modalities. Modalities are folded into the batch axis, so the backbone denoises each one as an independent sample and the adapters regroup them to attend across modalities, with absent modalities masked out of both attention and loss. This design gives the model flexibility in training and at inference. It trains directly on incomplete data and on unions of datasets, and at inference it either generates complete multimodal sets from noise or completes any missing subset from any observed one, using steering strategies rather than pattern-specific training.

#### Applications

Targeted two complementary uses in medical imaging. Co-generated multimodal studies can augment scarce datasets for downstream models such as tumor segmentation, and unacquired sequences can be completed from a patient’s partial MRI examination, with all synthesized modalities kept mutually consistent. Trained on a union of MRI datasets, the model can also synthesize modality combinations that no single subject contains. Because nothing in the design is specific to MRI, the same approach has been validated on both 2D natural images and 3D brain MRI, offering a general joint-distribution route to multimodal generation that addresses data scarcity and incomplete modalities across medical and non-medical domains.
