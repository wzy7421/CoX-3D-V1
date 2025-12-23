CoX-3D

Explainable Generative 3D Design Driven by Social Media Semantics

This repository provides a reference PyTorch implementation of the CoX-3D framework, an explainable, semantic-driven approach for generative 3D design based on large-scale social media data.

CoX-3D is designed to transform noisy, unstructured user-generated content (UGC) into interpretable design semantics, and further map these semantics into controllable 3D geometry and material representations through an explainable generation pipeline.

1. Overview

Social media platforms continuously generate large volumes of multimodal user expressions reflecting preferences, aesthetics, and experiential feedback. However, such data are not equivalent to explicit design requirements and are often highly noisy, emotional, and context-dependent.

CoX-3D addresses this challenge by:

Treating social media expressions as demand cues, rather than direct requirements;

Introducing an Explainable 3D Large Language Model (ELLM) to abstract, filter, and validate design-relevant semantics;

Integrating cross-modal semantic alignment, SDS-guided 3D optimization, and Mesh-VAE-PBR modeling;

Providing explainable feedback mechanisms (e.g., SHAP and Grad-CAM) to support human–AI collaborative design.

The framework is described in detail in the accompanying manuscript and Supplementary Information.

2. Methodological Positioning

Important:
This repository is not intended to be a production-level 3D asset generator.

Instead, it provides:

A methodological and algorithmic reference implementation of the CoX-3D framework;

Explicit correspondence to Figure 7, Algorithm 1–2, and equations in the paper;

Clear module boundaries enabling reproducibility, inspection, and extension.

The implementation focuses on semantic abstraction, optimization logic, and explainability, rather than industrial-scale rendering quality.

3. Repository Structure
cox3d/
├── core/                       # Paper-level framework (algorithmic abstraction)
│   ├── datasets/               # UGC dataset construction & preprocessing
│   ├── semantics/              # ELLM (BERTopic–LLM, semantic filtering)
│   ├── alignment/              # CLIP-based cross-modal alignment
│   ├── generation/             # SDS, NeRF abstraction, Mesh-VAE-PBR
│   ├── explain/                # SHAP & Grad-CAM explainability
│   └── engine/                 # End-to-end optimization logic
│
├── instantiations/
│   └── minimal_shapee/         # Minimal runnable instantiation
│       ├── generate_obj.py     # Text → 3D → textured OBJ
│       └── README.md
│
└── README.md                   # (this file)

4. Minimal Runnable Instantiation

To support practical verification and reproducibility, we provide a minimal runnable instantiation of the CoX-3D generation module based on an existing text-to-3D diffusion model.

Purpose of the Instantiation

Demonstrates semantic → 3D → textured mesh end-to-end execution;

Produces explicit 3D assets (OBJ + MTL + PNG) that can be opened in standard tools (e.g., Blender);

Serves as a concrete instantiation of the abstract CoX-3D generation pipeline.

This instantiation does not redefine the CoX-3D framework,
but rather materializes one feasible execution path of its generation module.

Location
instantiations/minimal_shapee/


Please refer to the README in that folder for detailed instructions.

5. Reproducibility Scope

The codebase enables reproduction of the following aspects:

Social media data structuring and semantic abstraction;

Topic-level semantic filtering with LLM guidance;

Cross-modal semantic alignment;

SDS-guided 3D optimization logic;

Mesh latent modeling and explainable feedback mechanisms;

End-to-end semantic-to-geometry mapping.

The repository intentionally decouples abstract methodology from specific generator implementations, allowing alternative instantiations to be plugged in.

6. Relation to the Paper

This repository corresponds to:

Figure 7 (overall framework and module interaction);

Algorithm 1 (CoX-3D dataset construction);

Algorithm 2 (end-to-end optimization and generation);

Methods and Supplementary Information sections on:

Semantic modeling (ELLM),

Cross-modal alignment,

SDS-guided generation,

Mesh-VAE-PBR modeling,

Explainable analysis.

All variable naming, module design, and loss definitions follow the notation used in the paper.

7. Citation

If you use this code, please cite the associated paper:

@article{cox3d2025,
  title={Explainable generative 3D design driven by social media semantics},
  author={...},
  journal={Nature Communications},
  year={2025}
}

8. License

This project is released for research and academic use only.
Please refer to individual third-party libraries for their respective licenses.

9. Contact

For questions regarding the methodology or implementation, please contact the corresponding author listed in the paper.
