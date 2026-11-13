---
title: "AnySyn: A diffusion-based framework for multimodality synthetic tasks"
order: 1
image: /images/projects/Project1.png
additional_image: /images/projects/AnySyn-overview.png
additional_image_alt: "AnySyn overview showing joint generation, any-subset completion, and cross-dataset synthesis."
---

#### Formulation

Independent modality-specific generators do not explicitly capture cross-modal dependencies, while training separate conditional models for different observed and missing modality combinations becomes increasingly costly as the number of modalities grows. AnySyn addresses these limitations by unifying multimodal image generation and missing-modality completion through joint generative modeling. A single model generates coherent multimodal samples from noise or completes missing modalities from arbitrary observed subsets within a predefined modality set. Training accommodates both complete and partially observed samples, allowing datasets with overlapping modality coverage to contribute without requiring complete samples spanning the full modality union.

#### Method

Designed a shared generative backbone augmented with lightweight cross-modal adapters. Modality folding lets the backbone process different modalities through the same input interface, while adapters exchange local and global features across modalities. Availability-aware attention and masked supervision restrict learning to observed data, without requiring missing targets to be imputed beforehand. The framework supports both training from scratch and parameter-efficient adaptation of pretrained models, including MAISI with its backbone frozen and only the adapters trained. During sampling, target modalities are updated jointly, while available observations guide completion without retraining for different input combinations.

#### Applications

Targeted complementary applications in medical imaging: generating multimodal 3D MRI, completing unacquired sequences from partial examinations, and jointly synthesizing MRI volumes and tumor masks for downstream segmentation. Joint training on MR-RATE and BraTS enables completion of modalities absent from one dataset but observed in another, using each subject’s available scans as conditions. Additional experiments on indoor scenes and multiview digits examine the framework beyond medical imaging. These applications address data scarcity and heterogeneous modality availability through a unified approach to multimodal generation and completion.
