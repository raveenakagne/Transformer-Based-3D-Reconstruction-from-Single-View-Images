# Transformer-Based 3D Reconstruction from Single-View Images

## Overview

This repository presents a modular pipeline for reconstructing 3D scenes from single-view RGB images using transformer-based models and generative AI. The framework integrates vision-language models, segmentation transformers, depth estimation techniques, and point cloud processing to generate high-fidelity 3D scaffolds. It is designed for applications in autonomous navigation, urban planning, and immersive environments.

## Features

- Transformer-based segmentation and depth estimation
- Vision-language captioning for semantic understanding
- Generative inpainting to recover occluded regions
- Point cloud generation and mesh reconstruction using Open3D
- Evaluation on the Cityscapes dataset with SSIM-based metrics

## Pipeline Architecture
<img width="1194" height="535" alt="image" src="https://github.com/user-attachments/assets/feac6b2c-ba8e-482a-9fdf-fdb515a45409" />

## Technologies Used

| Component         | Model/Tool                  | Purpose                                      |
|------------------|-----------------------------|----------------------------------------------|
| Captioning       | BLIP, LLaVA                 | Semantic understanding of image content      |
| Segmentation     | OneFormer                   | Multi-task segmentation (semantic, instance) |
| Inpainting       | Stable Diffusion 3.5        | Filling occluded/missing regions             |
| Depth Estimation | MiDaS, Depth Pro, DepthAnything V2 | Monocular depth prediction             |
| 3D Processing    | Open3D                      | Point cloud and mesh generation              |

## Dataset

**Cityscapes Dataset**

- 5000+ urban street-level images (1024×2048 resolution)
- Fine-grained pixel annotations across 30 categories
- Used for segmentation, depth estimation, and reconstruction validation

## Evaluation Metrics

- **SSIM (Structural Similarity Index Measure)**  
  Stable Diffusion 3.5 achieved an average SSIM of **0.48**, outperforming Runway ML in visual coherence.
  
- **Point Cloud Density**  
  Approximately **500,000 points** used per image for mesh generation.

## Results

- Improved structural fidelity and visual coherence in reconstructed 3D scenes
- Effective handling of occlusions and partial views
- High-quality depth maps and point clouds for urban environments

## Future Work

- **Integration of multimodal sensory data**  
  Incorporate additional inputs such as LiDAR and infrared imaging to improve reconstruction accuracy in low-light or complex environments.

- **Enhanced multiview consistency sampling**  
  Apply techniques that maintain spatial coherence across generated views, even when starting from a single image, to improve 3D model fidelity.

- **Optimization for low-resource environments**  
  Streamline the pipeline and model selection to support deployment on devices with limited computational power, enabling broader accessibility.

## Detail Overview 
- Transformer_Based_3D_Reconstruction_from_Single_view_Images.pdf is our IEEE format report explaining all the findings.
