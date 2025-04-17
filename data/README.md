# 📁 Data Folder – BrainScan AI

This folder contains preprocessed and metadata-linked datasets used for brain tumor detection and segmentation.

---

## 🧠 Folder Contents

### 🔹 `tumor_metadata.csv`
- Metadata for 3064 MRI scans with brain tumors.
- Each row corresponds to a single image derived from a `.mat` file in the original Figshare dataset.
- Includes:
  - `file`: Image filename (e.g., `1102.png`)
  - `label`: Numeric tumor type (1 = meningioma, 2 = glioma, 3 = pituitary)
  - `has_mask`: Boolean indicating if a binary mask exists
  - `tumorBorder`: Coordinates outlining the tumor (used for overlays)
  - `label_name`: Human-readable tumor type (e.g., `"glioma"`)

## 🧬 Source

- Data extracted and parsed from the original `.mat` files in the [Figshare Brain Tumor Dataset](https://figshare.com/articles/dataset/brain_tumor_dataset/1512427?file=51340418).
- Healthy MRI scans extracted from the original '.nii' files in the [IXI dataset- T1 Images](https://brain-development.org/ixi-dataset/?utm_source=chatgpt.com)
- Tumor masks and borders were extracted using `h5py` for figshare dataset and saved as PNG overlays.

---

## 📌 Usage

Use this metadata file to:
- Link PNG images to tumor types.
- Load tumor borders for visualization or weak supervision.
- Prepare datasets for classification, segmentation, or detection tasks.

---
