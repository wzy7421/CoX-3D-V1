===============================================================
CoX-3D: Explainable Generative 3D Design Driven by Social Media
===============================================================

This archive contains the software package accompanying the manuscript
“Explainable Generative 3D Design Driven by Social Media Semantics”
(under review at *Nature Communications*).

----------------------------------------------------------------
1. CONTENTS
----------------------------------------------------------------
- README.md .......... Detailed documentation (Markdown)
- readme.txt ......... This short plain-text overview
- LICENSE ............ MIT License file
- requirements.txt ... Python dependencies (minimal)
- configs/ ........... Demo and ablation configuration files
- docs/ .............. Reproduction guide and figure sources
- examples/ .......... Sample data (sample_data.zip)
- scripts/ ........... Utility scripts (e.g., download_models.sh)
- src/ ............... Python source code (pipeline stubs)
- static/ ............ Static project website (index.html + assets)
- tools/ ............. Main demo and utility scripts

----------------------------------------------------------------
2. INSTALLATION
----------------------------------------------------------------
1) Create a virtual environment:
   Windows (PowerShell):
     python -m venv .venv
     .venv\Scripts\Activate.ps1

   Linux/macOS:
     python3 -m venv .venv
     source .venv/bin/activate

2) Install required dependencies:
     pip install -r requirements.txt

----------------------------------------------------------------
3. QUICKSTART DEMO
----------------------------------------------------------------
Run a minimal end-to-end demo with provided sample data:

   python tools/demo.py --mode ti2d --config configs/cox3d_demo.yaml \
     --input_text "retro-futuristic hair dryer with matte finish" \
     --input_image examples/sample_data/images/ref_01.jpg \
     --save_cam --multi_view 4

Outputs will appear in:
   runs/demo/images/   -> multi-view and heatmap overlays
   runs/demo/meshes/   -> dummy OBJ mesh
   runs/demo/reports/  -> JSON metrics

----------------------------------------------------------------
4. DATA AVAILABILITY
----------------------------------------------------------------
- Public datasets: COCO 2017, KITTI (not redistributed here).
- Minimal sample data is included in examples/sample_data.zip.
- Full in-house datasets cannot be shared due to restrictions.
  See DATA_AVAILABILITY.md for details.

----------------------------------------------------------------
5. REPRODUCIBILITY
----------------------------------------------------------------
- Steps for reproducing paper figures and tables are documented in
  docs/reproduction.md
- Minimal demo is sufficient for reviewers to verify pipeline
  installation and execution.

----------------------------------------------------------------
6. LICENSE & CONTACT
----------------------------------------------------------------
- License: MIT (see LICENSE)
- Maintainer: Zhenyu Wang (Tongji University)
- Email: 2411673@tongji.edu.cn
- ORCID: https://orcid.org/0000-0001-7645-5667

----------------------------------------------------------------
END OF FILE
----------------------------------------------------------------
