# esri-toolbox-calculate-svf-from-streetviewpanorama


# Street View Panorama to Fisheye Toolbox

This repository contains an ArcGIS Python Toolbox (`googlestreetview_to_fisheye.pyt`) for:
- Downloading Google Street View panoramas for given point along with panoid and lat, lon
- Converting to fisheye projections
- Estimating Sky View Factor (SVF) using Segment Anything (SAM)

---

## 🔽 Download SAM model weights

This toolbox requires the [Segment Anything](https://github.com/facebookresearch/segment-anything) model weights.

Please download **`sam_vit_h_4b8939.pth`** from the official release:

👉 [Download from Meta AI](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth)

---

## 📂 Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/streetview-fisheye-svf.git
   cd streetview-fisheye-svf```
   
   
2. Create a folder named models inside the repo:

```mkdir models```

3. Move the downloaded checkpoint into the models folder:

```models/sam_vit_h_4b8939.pth```

Your final structure should look like:

```streetview-fisheye-svf/
│── googlestreetview_to_fisheye.pyt
│── README.md
└── models/
    └── sam_vit_h_4b8939.pth
```
	

4. clone new env from base arcgispy3 env in arcgis pro package manager interface	

5. select cloned env as activate env

6. check activated env is selected to be sure from View > Python Windows

Enter:

```import sys
import os
print(sys.version)
print(os.environ.get("CONDA_DEFAULT_ENV"))
print(sys.path[:3])  # show first 3 search paths
```

It should be pointing your freshly cloned env.

7. Open Python Command Promt

Install via pip package manager(check your cuda version with "nvidia-smi" in terminal):
```
pip install opencv-python --no-deps
pip3 install torch torchvision --index-url https://download.pytorch.org/whl/cu126
```
