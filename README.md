# Soccer-Reid

An end-to-end solution to consistently identify soccer players across two camera feeds (“broadcast” and “tacticam”) using:

1. **Object Detection & Tracking** (YOLOv11 + DeepSORT)  
2. **Appearance Feature Extraction** (OSNet-AIN person ReID)  
3. **Cross-Camera Matching** (cosine similarity + Hungarian algorithm)

## 🚀 Features

- **Robust Detection & Tracking**  
  - Detects players & referees per frame  
  - Assigns consistent intra-video IDs  
  - Annotates and saves output videos  

- **Appearance Embeddings**  
  - Extracts 512-dim person embeddings  
  - Averages per-track embeddings  
  - Saves feature JSONs for downstream matching  

- **Optimal Matching**  
  - Computes full pairwise cosine similarities  
  - Uses the Hungarian algorithm for 1:1 assignment  
  - Exports final ID mapping (tacticam → broadcast)

- **Modular & Extensible**  
  - Three standalone scripts (`part1`, `part2`, `part3`)  
  - Configurable confidence thresholds and parameters  
  - Easily swap models or integrate additional cues (jersey OCR, homography, etc.)

---
