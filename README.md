
# CoX‑3D: Explainable Generative 3D Design Driven by Social Media Semantics

This repository accompanies the manuscript **“Explainable Generative 3D Design Driven by Social Media Semantics”** (under review at *Nature Communications*). It provides runnable code, example inputs, and instructions to reproduce the main results.

**TL;DR.** CoX‑3D is an end‑to‑end pipeline that turns UGC‑derived requirements into manufacturable 3D models through: (R1) requirement modeling, (R2) multimodal prompt engineering, (R3) 3D generation + DfM checks, and (R4) interpretable optimization.

## Quickstart
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python tools/demo.py --mode ti2d --config configs/cox3d_demo.yaml --input_text "retro-futuristic hair dryer" --input_image examples/sample_data/images/ref_01.jpg --save_cam --multi_view 4
```
See `docs/reproduction.md` for figure/table mapping. Minimal sample data is provided in `examples/sample_data.zip`.

## Reproducibility
- Machine Learning Checklist (Nature): https://www.nature.com/documents/machine-learning-checklist.pdf
- Software/Custom Code Checklist (Nature): https://www.nature.com/documents/nr-software-policy.pdf
- Data availability: see `DATA_AVAILABILITY.md`

## Citation
```
@article{wang2025cox3d,
  title   = {Explainable Generative 3D Design Driven by Social Media Semantics},
  author  = {Wang, Zhenyu and Sato, Karen and Wang, Jianmin},
  journal = {Under review at Nature Communications},
  year    = {2025},
  url     = {https://github.com/REPLACE_WITH_YOUR_ORG/CoX-3D}
}
```
